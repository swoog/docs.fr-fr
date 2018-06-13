---
title: ICorProfilerCallback::JITInlining, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.JITInlining
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::JITInlining
helpviewer_keywords:
- JITInlining method [.NET Framework profiling]
- ICorProfilerCallback::JITInlining method [.NET Framework profiling]
ms.assetid: c2f45801-dd38-4b78-b6b7-64397dc73f83
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 844ac2a8aad4ce2cc6f70de2d5a53c7c0b6f4f6c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33453142"
---
# <a name="icorprofilercallbackjitinlining-method"></a><span data-ttu-id="432b0-102">ICorProfilerCallback::JITInlining, méthode</span><span class="sxs-lookup"><span data-stu-id="432b0-102">ICorProfilerCallback::JITInlining Method</span></span>
<span data-ttu-id="432b0-103">Notifie le profileur que le compilateur juste-à-temps (JIT) est sur le point d’insertion d’une fonction conformément à une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="432b0-103">Notifies the profiler that the just-in-time (JIT) compiler is about to insert a function in line with another function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="432b0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="432b0-104">Syntax</span></span>  
  
```  
HRESULT JITInlining(  
    [in]  FunctionID callerId,  
    [in]  FunctionID calleeId,  
    [out] BOOL      *pfShouldInline);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="432b0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="432b0-105">Parameters</span></span>  
 `callerId`  
 <span data-ttu-id="432b0-106">[in] L’ID de la fonction dans laquelle le `calleeId` fonction sera insérée.</span><span class="sxs-lookup"><span data-stu-id="432b0-106">[in] The ID of the function into which the `calleeId` function will be inserted.</span></span>  
  
 `calleeId`  
 <span data-ttu-id="432b0-107">[in] L’ID de la fonction à insérer.</span><span class="sxs-lookup"><span data-stu-id="432b0-107">[in] The ID of the function to be inserted.</span></span>  
  
 `pfShouldInline`  
 <span data-ttu-id="432b0-108">[out] `true` pour permettre l’insertion ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="432b0-108">[out] `true` to allow the insertion to occur; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="432b0-109">Notes</span><span class="sxs-lookup"><span data-stu-id="432b0-109">Remarks</span></span>  
 <span data-ttu-id="432b0-110">Le profileur peut affecter `pfShouldInline` à `false` pour empêcher la `calleeId` fonction à partir de laquelle elle est insérée la `callerId` (fonction).</span><span class="sxs-lookup"><span data-stu-id="432b0-110">The profiler can set `pfShouldInline` to `false` to prevent the `calleeId` function from being inserted into the `callerId` function.</span></span> <span data-ttu-id="432b0-111">En outre, le profileur peut désactiver globalement l’insertion d’inline à l’aide de la valeur COR_PRF_DISABLE_INLINING de le [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="432b0-111">Also, the profiler can globally disable inline insertion by using the COR_PRF_DISABLE_INLINING value of the [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
 <span data-ttu-id="432b0-112">Insérer les fonctions inline ne déclenchent pas d’événements pour l’entrée ou la sortie.</span><span class="sxs-lookup"><span data-stu-id="432b0-112">Functions inserted inline do not raise events for entering or leaving.</span></span> <span data-ttu-id="432b0-113">Par conséquent, le profileur doit affecter `pfShouldInline` à `false` afin de produire un graphique des appels précis.</span><span class="sxs-lookup"><span data-stu-id="432b0-113">Therefore, the profiler must set `pfShouldInline` to `false` in order to produce an accurate callgraph.</span></span> <span data-ttu-id="432b0-114">Paramètre `pfShouldInline` à `false` affecte les performances, car l’insertion inline généralement augmente la vitesse et réduit le nombre d’événements de compilation JIT séparés pour la méthode insérée.</span><span class="sxs-lookup"><span data-stu-id="432b0-114">Setting `pfShouldInline` to `false` will affect performance, because inline insertion typically increases speed and reduces the number of separate JIT compilation events for the inserted method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="432b0-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="432b0-115">Requirements</span></span>  
 <span data-ttu-id="432b0-116">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="432b0-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="432b0-117">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="432b0-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="432b0-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="432b0-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="432b0-119">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="432b0-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="432b0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="432b0-120">See Also</span></span>  
 [<span data-ttu-id="432b0-121">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="432b0-121">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
