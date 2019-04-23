---
title: FunctionIDMapper2, fonction
ms.date: 03/30/2017
api_name:
- FunctionIDMapper2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionIDMapper2
helpviewer_keywords:
- FunctionIDMapper2 function [.NET Framework profiling]
ms.assetid: 466ad51b-8f0c-41d9-81f7-371aac3374cb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1a236dcae29d00afe3b72dce8f81d657fb4fac28
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59082501"
---
# <a name="functionidmapper2-function"></a><span data-ttu-id="faa40-102">FunctionIDMapper2, fonction</span><span class="sxs-lookup"><span data-stu-id="faa40-102">FunctionIDMapper2 Function</span></span>
<span data-ttu-id="faa40-103">Notifie le profileur que l’identificateur donné d’une fonction peut être remappé vers un autre ID à utiliser dans le [FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md), [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md), et [FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md), ou[FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md), [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md), et [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) rappels pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="faa40-103">Notifies the profiler that the given identifier of a function may be remapped to an alternative ID to be used in the [FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md), [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md), and [FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md), or[FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md), [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md), and [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) callbacks for that function.</span></span> <span data-ttu-id="faa40-104">`FunctionIDMapper2` permet également au profileur d'indiquer s'il souhaite recevoir des rappels pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="faa40-104">`FunctionIDMapper2` also enables the profiler to indicate whether it wants to receive callbacks for that function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="faa40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="faa40-105">Syntax</span></span>  
  
```  
UINT_PTR __stdcall FunctionIDMapper2 (  
    [in]  FunctionID  funcId,  
    [in]  void * clientData,  
    [out] BOOL       *pbHookFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="faa40-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="faa40-106">Parameters</span></span>  
 `funcId`  
 <span data-ttu-id="faa40-107">[in] Identificateur de fonction à remapper.</span><span class="sxs-lookup"><span data-stu-id="faa40-107">[in] The function identifier to be remapped.</span></span>  
  
 `clientData`  
 <span data-ttu-id="faa40-108">[in] Pointeur vers les données utilisées pour distinguer les différents runtimes.</span><span class="sxs-lookup"><span data-stu-id="faa40-108">[in] A pointer to data that is used to disambiguate among runtimes.</span></span>  
  
 `pbHookFunction`  
 <span data-ttu-id="faa40-109">[out] Pointeur vers une valeur à laquelle le profileur affecte `true` s'il souhaite recevoir des rappels `FunctionEnter3`, `FunctionLeave3` et `FunctionTailcall3` ou `FunctionEnter3WithInfo`, `FunctionLeave3WithInfo` et `FunctionTailcall3WithInfo` ; sinon, il affecte `false` à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="faa40-109">[out] A pointer to a value that the profiler sets to `true` if it wants to receive `FunctionEnter3`, `FunctionLeave3`, and `FunctionTailcall3`, or `FunctionEnter3WithInfo`, `FunctionLeave3WithInfo`, and `FunctionTailcall3WithInfo` callbacks; otherwise, it sets this value to `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="faa40-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="faa40-110">Return Value</span></span>  
 <span data-ttu-id="faa40-111">Le profileur retourne une valeur que le moteur d'exécution utilise comme autre identificateur de fonction.</span><span class="sxs-lookup"><span data-stu-id="faa40-111">The profiler returns a value that the execution engine uses as an alternative function identifier.</span></span> <span data-ttu-id="faa40-112">La valeur de retour ne peut pas être null, sauf si `false` est retourné dans `pbHookFunction`.</span><span class="sxs-lookup"><span data-stu-id="faa40-112">The return value cannot be null unless `false` is returned in `pbHookFunction`.</span></span> <span data-ttu-id="faa40-113">Sinon, une valeur de retour null génère des résultats imprévisibles pouvant aller jusqu'à l'arrêt du processus.</span><span class="sxs-lookup"><span data-stu-id="faa40-113">Otherwise, a null return value produces unpredictable results, including possibly halting the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="faa40-114">Notes</span><span class="sxs-lookup"><span data-stu-id="faa40-114">Remarks</span></span>  
 <span data-ttu-id="faa40-115">Cette méthode étend la [FunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md) fonction avec un paramètre supplémentaire qui est utilisé pour passer des données client.</span><span class="sxs-lookup"><span data-stu-id="faa40-115">This method extends the [FunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md) function with an additional parameter that is used to pass client data.</span></span> <span data-ttu-id="faa40-116">Les données client sont utilisées pour distinguer les différents runtimes.</span><span class="sxs-lookup"><span data-stu-id="faa40-116">The client data is used to disambiguate among runtimes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="faa40-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faa40-117">Requirements</span></span>  
 <span data-ttu-id="faa40-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="faa40-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="faa40-119">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="faa40-119">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="faa40-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="faa40-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="faa40-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="faa40-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="faa40-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="faa40-122">See also</span></span>

- [<span data-ttu-id="faa40-123">ICorProfilerInfo::SetFunctionIDMapper</span><span class="sxs-lookup"><span data-stu-id="faa40-123">ICorProfilerInfo::SetFunctionIDMapper</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setfunctionidmapper-method.md)
- [<span data-ttu-id="faa40-124">ICorProfilerInfo3::SetFunctionIDMapper2</span><span class="sxs-lookup"><span data-stu-id="faa40-124">ICorProfilerInfo3::SetFunctionIDMapper2</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setfunctionidmapper2-method.md)
- [<span data-ttu-id="faa40-125">FunctionEnter3</span><span class="sxs-lookup"><span data-stu-id="faa40-125">FunctionEnter3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md)
- [<span data-ttu-id="faa40-126">FunctionLeave3</span><span class="sxs-lookup"><span data-stu-id="faa40-126">FunctionLeave3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md)
- [<span data-ttu-id="faa40-127">FunctionTailcall3</span><span class="sxs-lookup"><span data-stu-id="faa40-127">FunctionTailcall3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md)
- [<span data-ttu-id="faa40-128">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="faa40-128">FunctionEnter3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md)
- [<span data-ttu-id="faa40-129">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="faa40-129">FunctionLeave3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md)
- [<span data-ttu-id="faa40-130">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="faa40-130">FunctionTailcall3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)
- [<span data-ttu-id="faa40-131">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="faa40-131">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
