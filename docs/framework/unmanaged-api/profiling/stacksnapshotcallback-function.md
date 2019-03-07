---
title: StackSnapshotCallback (fonction)
ms.date: 03/30/2017
api_name:
- StackSnapshotCallback
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- StackSnapshotCallback
helpviewer_keywords:
- StackSnapshotCallback function [.NET Framework profiling]
ms.assetid: d0f235b2-91fe-4f82-b7d5-e5c64186eea8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 43e71696282a3c9e6d25793b583ee19f306e167b
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57486236"
---
# <a name="stacksnapshotcallback-function"></a><span data-ttu-id="3ac42-102">StackSnapshotCallback (fonction)</span><span class="sxs-lookup"><span data-stu-id="3ac42-102">StackSnapshotCallback Function</span></span>
<span data-ttu-id="3ac42-103">Fournit au profileur des informations sur chaque frame managé et chaque exécution de trames non gérées sur la pile pendant un parcours de pile, ce qui est lancée par le [ICorProfilerInfo2::DoStackSnapshot](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-dostacksnapshot-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="3ac42-103">Provides the profiler with information about each managed frame and each run of unmanaged frames on the stack during a stack walk, which is initiated by the [ICorProfilerInfo2::DoStackSnapshot](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-dostacksnapshot-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3ac42-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ac42-104">Syntax</span></span>  
  
```  
HRESULT __stdcall StackSnapshotCallback (  
    [in] FunctionID funcId,  
    [in] UINT_PTR ip,  
    [in] COR_PRF_FRAME_INFO frameInfo,  
    [in] ULONG32 contextSize,  
    [in] BYTE context[],  
    [in] void *clientData  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3ac42-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ac42-105">Parameters</span></span>  
 `funcId`  
 <span data-ttu-id="3ac42-106">[in] Si cette valeur est zéro, ce rappel est pour une exécution de trames non gérées ; Sinon, il est l’identificateur d’une fonction managée et ce rappel est pour une trame gérée.</span><span class="sxs-lookup"><span data-stu-id="3ac42-106">[in] If this value is zero, this callback is for a run of unmanaged frames; otherwise, it is the identifier of a managed function and this callback is for a managed frame.</span></span>  
  
 `ip`  
 <span data-ttu-id="3ac42-107">[in] La valeur de pointeur d’instruction de code natif dans le cadre.</span><span class="sxs-lookup"><span data-stu-id="3ac42-107">[in] The value of the native code instruction pointer in the frame.</span></span>  
  
 `frameInfo`  
 <span data-ttu-id="3ac42-108">[in] Un `COR_PRF_FRAME_INFO` valeur qui fait référence aux informations sur le frame de pile.</span><span class="sxs-lookup"><span data-stu-id="3ac42-108">[in] A `COR_PRF_FRAME_INFO` value that references information about the stack frame.</span></span> <span data-ttu-id="3ac42-109">Cette valeur est valide pour une utilisation uniquement pendant ce rappel.</span><span class="sxs-lookup"><span data-stu-id="3ac42-109">This value is valid for use only during this callback.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="3ac42-110">[in] La taille de la `CONTEXT` structure, ce qui est référencé par le `context` paramètre.</span><span class="sxs-lookup"><span data-stu-id="3ac42-110">[in] The size of the `CONTEXT` structure, which is referenced by the `context` parameter.</span></span>  
  
 `context`  
 <span data-ttu-id="3ac42-111">[in] Un pointeur vers un Win32 `CONTEXT` structure qui représente l’état de l’UC pour ce frame.</span><span class="sxs-lookup"><span data-stu-id="3ac42-111">[in] A pointer to a Win32 `CONTEXT` structure that represents the state of the CPU for this frame.</span></span>  
  
 <span data-ttu-id="3ac42-112">Le `context` paramètre est valide uniquement si l’indicateur COR_PRF_SNAPSHOT_CONTEXT a été passé dans `ICorProfilerInfo2::DoStackSnapshot`.</span><span class="sxs-lookup"><span data-stu-id="3ac42-112">The `context` parameter is valid only if the COR_PRF_SNAPSHOT_CONTEXT flag was passed in `ICorProfilerInfo2::DoStackSnapshot`.</span></span>  
  
 `clientData`  
 <span data-ttu-id="3ac42-113">[in] Un pointeur vers les données client, qui sont ensuite transmis directement à partir de `ICorProfilerInfo2::DoStackSnapshot`.</span><span class="sxs-lookup"><span data-stu-id="3ac42-113">[in] A pointer to the client data, which is passed straight through from `ICorProfilerInfo2::DoStackSnapshot`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3ac42-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3ac42-114">Remarks</span></span>  
 <span data-ttu-id="3ac42-115">Le `StackSnapshotCallback` fonction est implémentée par le writer de profileur.</span><span class="sxs-lookup"><span data-stu-id="3ac42-115">The `StackSnapshotCallback` function is implemented by the profiler writer.</span></span> <span data-ttu-id="3ac42-116">Vous devez limiter la complexité du travail effectué dans `StackSnapshotCallback`.</span><span class="sxs-lookup"><span data-stu-id="3ac42-116">You must limit the complexity of work done in `StackSnapshotCallback`.</span></span> <span data-ttu-id="3ac42-117">Par exemple, lorsque vous utilisez `ICorProfilerInfo2::DoStackSnapshot` de manière asynchrone, le thread cible peut contenir des verrous.</span><span class="sxs-lookup"><span data-stu-id="3ac42-117">For example, when using `ICorProfilerInfo2::DoStackSnapshot` in an asynchronous manner, the target thread may be holding locks.</span></span> <span data-ttu-id="3ac42-118">Si le code situé dans `StackSnapshotCallback` requiert les mêmes verrous, un interblocage susceptibles d’en découler.</span><span class="sxs-lookup"><span data-stu-id="3ac42-118">If code within `StackSnapshotCallback` requires the same locks, a deadlock could ensue.</span></span>  
  
 <span data-ttu-id="3ac42-119">Le `ICorProfilerInfo2::DoStackSnapshot` les appels de méthode le `StackSnapshotCallback` fonction une fois par trame gérée ou une fois par exécution de trames non gérées.</span><span class="sxs-lookup"><span data-stu-id="3ac42-119">The `ICorProfilerInfo2::DoStackSnapshot` method calls the `StackSnapshotCallback` function once per managed frame or once per run of unmanaged frames.</span></span> <span data-ttu-id="3ac42-120">Si `StackSnapshotCallback` est appelée pour une exécution de trames non gérées, le profileur peut utiliser le contexte de Registre (référencé par le `context` paramètre) pour effectuer son propre parcours de pile non géré.</span><span class="sxs-lookup"><span data-stu-id="3ac42-120">If `StackSnapshotCallback` is called for a run of unmanaged frames, the profiler may use the register context (referenced by the `context` parameter) to perform its own unmanaged stack walk.</span></span> <span data-ttu-id="3ac42-121">Dans ce cas, Win32 `CONTEXT` structure représente l’état de l’UC pour le frame de la plus récemment envoyée lors de l’exécution de trames non gérées.</span><span class="sxs-lookup"><span data-stu-id="3ac42-121">In this case, the Win32 `CONTEXT` structure represents the CPU state for the most recently pushed frame within the run of unmanaged frames.</span></span> <span data-ttu-id="3ac42-122">Bien que Win32 `CONTEXT` structure inclut des valeurs pour tous les registres, vous devez utiliser uniquement les valeurs de Registre de pointeur de pile, Registre de pointeur de frame, Registre de pointeur d’instruction et la non volatile (qui est, conservée) registres d’entiers.</span><span class="sxs-lookup"><span data-stu-id="3ac42-122">Although the Win32 `CONTEXT` structure includes values for all registers, you should rely only on the values of the stack pointer register, frame pointer register, instruction pointer register, and the nonvolatile (that is, preserved) integer registers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3ac42-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3ac42-123">Requirements</span></span>  
 <span data-ttu-id="3ac42-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3ac42-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3ac42-125">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="3ac42-125">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="3ac42-126">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3ac42-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3ac42-127">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3ac42-127">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ac42-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ac42-128">See also</span></span>
- [<span data-ttu-id="3ac42-129">DoStackSnapshot, méthode</span><span class="sxs-lookup"><span data-stu-id="3ac42-129">DoStackSnapshot Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-dostacksnapshot-method.md)
- [<span data-ttu-id="3ac42-130">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="3ac42-130">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
