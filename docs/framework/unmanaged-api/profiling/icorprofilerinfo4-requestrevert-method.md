---
title: ICorProfilerInfo4::RequestRevert, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.RequestRevert
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::RequestRevert
helpviewer_keywords:
- RequestRevert method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::RequestRevert method [.NET Framework profiling]
ms.assetid: 70261da5-5933-4e25-9de0-ddf51cba56cc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 92137e1a5b0923bc34745513715934c483616700
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62000491"
---
# <a name="icorprofilerinfo4requestrevert-method"></a><span data-ttu-id="d0705-102">ICorProfilerInfo4::RequestRevert, méthode</span><span class="sxs-lookup"><span data-stu-id="d0705-102">ICorProfilerInfo4::RequestRevert Method</span></span>
<span data-ttu-id="d0705-103">Rétablit les versions d'origine de toutes les instances des fonctions spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d0705-103">Reverts all instances of the specified functions to their original versions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d0705-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0705-104">Syntax</span></span>  
  
```  
HRESULT RequestRevert (  
   [in] ULONG    cFunctions,  
   [in, size_is(cFunctions)]  ModuleID    moduleIds[],  
   [in, size_is(cFunctions)]  mdMethodDef methodIds[],  
   [out, size_is(cFunctions)]  HRESULT status[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d0705-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0705-105">Parameters</span></span>  
 `cFunctions`  
 <span data-ttu-id="d0705-106">[in] Nombre de fonctions à rétablir.</span><span class="sxs-lookup"><span data-stu-id="d0705-106">[in] The number of functions to revert.</span></span>  
  
 `moduleIds`  
 <span data-ttu-id="d0705-107">[in] Spécifie la partie `moduleId` des paires (`module`, `methodDef`) qui identifient les fonctions à rétablir.</span><span class="sxs-lookup"><span data-stu-id="d0705-107">[in] Specifies the `moduleId` portion of the (`module`, `methodDef`) pairs that identify the functions to be reverted.</span></span>  
  
 `methodIds`  
 <span data-ttu-id="d0705-108">[in] Spécifie la partie `methodId` des paires (`module`, `methodDef`) qui identifient les fonctions à rétablir.</span><span class="sxs-lookup"><span data-stu-id="d0705-108">[in] Specifies the `methodId` portion of the (`module`, `methodDef`) pairs that identify the functions to be reverted.</span></span>  
  
 `status`  
 <span data-ttu-id="d0705-109">[out] Tableau de HRESULT répertoriés dans la section « HRESULT d'état » plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d0705-109">[out] An array of HRESULTs listed in the "Status HRESULTs" section later in this topic.</span></span> <span data-ttu-id="d0705-110">Chaque HRESULT indique la réussite ou l'échec de la tentative de rétablissement de chaque fonction spécifiée dans les tableaux parallèles `moduleIds` et `methodIds`.</span><span class="sxs-lookup"><span data-stu-id="d0705-110">Each HRESULT indicates the success or failure of trying to revert each function specified in the parallel arrays `moduleIds` and `methodIds`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d0705-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d0705-111">Return Value</span></span>  
 <span data-ttu-id="d0705-112">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="d0705-112">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="d0705-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d0705-113">HRESULT</span></span>|<span data-ttu-id="d0705-114">Description</span><span class="sxs-lookup"><span data-stu-id="d0705-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d0705-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0705-115">S_OK</span></span>|<span data-ttu-id="d0705-116">Une tentative de rétablissement de toutes les demandes a été effectuée ; toutefois, le tableau d'états retourné doit être examiné pour déterminer les fonctions qui ont été correctement rétablies.</span><span class="sxs-lookup"><span data-stu-id="d0705-116">An attempt was made to revert all requests; however, the returned status array must be checked to determine which functions were successfully reverted.</span></span>|  
|<span data-ttu-id="d0705-117">CORPROF_E_CALLBACK4_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="d0705-117">CORPROF_E_CALLBACK4_REQUIRED</span></span>|<span data-ttu-id="d0705-118">Le profileur doit implémenter le [ICorProfilerCallback4](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md) interface pour cet appel être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d0705-118">The profiler must implement the [ICorProfilerCallback4](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md) interface for this call to be supported.</span></span>|  
|<span data-ttu-id="d0705-119">CORPROF_E_REJIT_NOT_ENABLED</span><span class="sxs-lookup"><span data-stu-id="d0705-119">CORPROF_E_REJIT_NOT_ENABLED</span></span>|<span data-ttu-id="d0705-120">La recompilation juste-à-temps n'a pas été activée.</span><span class="sxs-lookup"><span data-stu-id="d0705-120">JIT recompilation has not been enabled.</span></span> <span data-ttu-id="d0705-121">Vous devez activer la recompilation JIT pendant l’initialisation à l’aide de la [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) méthode pour définir le `COR_PRF_ENABLE_REJIT` indicateur.</span><span class="sxs-lookup"><span data-stu-id="d0705-121">You must enable JIT recompilation during initialization by using the [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) method to set the `COR_PRF_ENABLE_REJIT` flag.</span></span>|  
|<span data-ttu-id="d0705-122">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d0705-122">E_INVALIDARG</span></span>|<span data-ttu-id="d0705-123">`cFunctions` est égal à 0, ou `moduleIds` ou `methodIds` a la valeur `NULL`.</span><span class="sxs-lookup"><span data-stu-id="d0705-123">`cFunctions` is 0, or `moduleIds` or `methodIds` is `NULL`.</span></span>|  
|<span data-ttu-id="d0705-124">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d0705-124">E_OUTOFMEMORY</span></span>|<span data-ttu-id="d0705-125">Le CLR n'a pas pu terminer la demande en raison d'une mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d0705-125">The CLR was unable to complete the request because it ran out of memory.</span></span>|  
  
## <a name="status-hresults"></a><span data-ttu-id="d0705-126">HRESULT d'état</span><span class="sxs-lookup"><span data-stu-id="d0705-126">Status HRESULTS</span></span>  
  
|<span data-ttu-id="d0705-127">HRESULT du tableau d'états</span><span class="sxs-lookup"><span data-stu-id="d0705-127">Status array HRESULT</span></span>|<span data-ttu-id="d0705-128">Description</span><span class="sxs-lookup"><span data-stu-id="d0705-128">Description</span></span>|  
|--------------------------|-----------------|  
|<span data-ttu-id="d0705-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0705-129">S_OK</span></span>|<span data-ttu-id="d0705-130">La fonction correspondante a été rétablie.</span><span class="sxs-lookup"><span data-stu-id="d0705-130">The corresponding function was successfully reverted.</span></span>|  
|<span data-ttu-id="d0705-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d0705-131">E_INVALIDARG</span></span>|<span data-ttu-id="d0705-132">Le paramètre `moduleID` ou `methodDef` est `NULL`.</span><span class="sxs-lookup"><span data-stu-id="d0705-132">The `moduleID` or `methodDef` parameter is `NULL`.</span></span>|  
|<span data-ttu-id="d0705-133">CORPROF_E_DATAINCOMPLETE</span><span class="sxs-lookup"><span data-stu-id="d0705-133">CORPROF_E_DATAINCOMPLETE</span></span>|<span data-ttu-id="d0705-134">Le module n'est pas encore totalement chargé ou il est en cours de déchargement.</span><span class="sxs-lookup"><span data-stu-id="d0705-134">The module is not fully loaded yet, or it is in the process of being unloaded.</span></span>|  
|<span data-ttu-id="d0705-135">CORPROF_E_MODULE_IS_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="d0705-135">CORPROF_E_MODULE_IS_DYNAMIC</span></span>|<span data-ttu-id="d0705-136">Le module spécifié a été généré dynamiquement (par exemple, par `Reflection.Emit`).</span><span class="sxs-lookup"><span data-stu-id="d0705-136">The specified module was dynamically generated (for example by `Reflection.Emit`).</span></span> <span data-ttu-id="d0705-137">Par conséquent, il n'est pas pris en charge par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d0705-137">Therefore, it is not supported by this method.</span></span>|  
|<span data-ttu-id="d0705-138">CORPROF_E_ACTIVE_REJIT_REQUEST_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d0705-138">CORPROF_E_ACTIVE_REJIT_REQUEST_NOT_FOUND</span></span>|<span data-ttu-id="d0705-139">Le CLR ne peut pas rétablir la fonction spécifiée, car une demande de recompilation active correspondante est introuvable.</span><span class="sxs-lookup"><span data-stu-id="d0705-139">The CLR could not revert the specified function, because a corresponding active recompilation request was not found.</span></span> <span data-ttu-id="d0705-140">La recompilation n'a jamais demandée ou la fonction a déjà été rétablie.</span><span class="sxs-lookup"><span data-stu-id="d0705-140">Either the recompilation was never requested or the function was already reverted.</span></span>|  
|<span data-ttu-id="d0705-141">Autre</span><span class="sxs-lookup"><span data-stu-id="d0705-141">Other</span></span>|<span data-ttu-id="d0705-142">Le système d'exploitation a retourné un échec en dehors du contrôle du CLR.</span><span class="sxs-lookup"><span data-stu-id="d0705-142">The operating system returned a failure outside the control of the CLR.</span></span> <span data-ttu-id="d0705-143">Par exemple, en cas d'échec d'un appel système visant à modifier la protection d'accès d'une page de mémoire, l'erreur du système d'exploitation s'affiche.</span><span class="sxs-lookup"><span data-stu-id="d0705-143">For example, if a system call to change the access protection of a page of memory fails, the operating system error will be displayed.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d0705-144">Notes</span><span class="sxs-lookup"><span data-stu-id="d0705-144">Remarks</span></span>  
 <span data-ttu-id="d0705-145">Lors du prochain appel des instances de la fonction rétablie, les versions d'origine des fonctions seront exécutées.</span><span class="sxs-lookup"><span data-stu-id="d0705-145">The next time any of the revereted function instances are called, the original versions of the functions will be run.</span></span> <span data-ttu-id="d0705-146">Si une fonction est déjà en cours d'exécution, il termine l'exécution de la version en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="d0705-146">If a function is already running, it will finish executing the version that is running.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d0705-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0705-147">Requirements</span></span>  
 <span data-ttu-id="d0705-148">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d0705-148">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0705-149">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d0705-149">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d0705-150">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d0705-150">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d0705-151">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d0705-151">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0705-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0705-152">See also</span></span>

- [<span data-ttu-id="d0705-153">ICorProfilerInfo4, interface</span><span class="sxs-lookup"><span data-stu-id="d0705-153">ICorProfilerInfo4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)
- [<span data-ttu-id="d0705-154">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="d0705-154">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="d0705-155">Profilage</span><span class="sxs-lookup"><span data-stu-id="d0705-155">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
