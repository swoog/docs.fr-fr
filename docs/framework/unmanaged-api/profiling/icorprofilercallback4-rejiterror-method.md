---
title: ICorProfilerCallback4::ReJITError, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback4.ReJITError
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback4::ReJITError
helpviewer_keywords:
- ReJITError method, ICorProfilerCallback4 interface [.NET Framework profiling]
- ICorProfilerCallback4::ReJITError method [.NET Framework profiling]
ms.assetid: d7888aa9-dfaa-420f-9f99-e06ab35ca482
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e0cd68f5a15bbd8942f0dc889ecb74b7fde00d30
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57502319"
---
# <a name="icorprofilercallback4rejiterror-method"></a><span data-ttu-id="f595e-102">ICorProfilerCallback4::ReJITError, méthode</span><span class="sxs-lookup"><span data-stu-id="f595e-102">ICorProfilerCallback4::ReJITError Method</span></span>
<span data-ttu-id="f595e-103">Notifie le profileur que compilateur juste-à-temps (JIT) a rencontré une erreur dans le processus de recompilation.</span><span class="sxs-lookup"><span data-stu-id="f595e-103">Notifies the profiler that the just-in-time (JIT) compiler encountered an error in the recompilation process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f595e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f595e-104">Syntax</span></span>  
  
```  
HRESULT ReJITError(  
    [in] ModuleID    moduleId,  
    [in] mdMethodDef methodId,  
    [in] FunctionID  functionId,  
    [in] HRESULT     hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f595e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f595e-105">Parameters</span></span>  
 `moduleID`  
 <span data-ttu-id="f595e-106">[in] Le `ModuleID` dans lequel la tentative de recompilation ayant échoué a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="f595e-106">[in] The `ModuleID` in which the failed recompilation attempt was made.</span></span>  
  
 `methodId`  
 <span data-ttu-id="f595e-107">[in] Le `MethodDef` de la méthode sur lequel la tentative de recompilation ayant échoué a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="f595e-107">[in] The `MethodDef` of the method on which the failed recompilation attempt was made.</span></span>  
  
 `functionId`  
 <span data-ttu-id="f595e-108">[in] L’instance de fonction qui est en cours de recompilation recompilée ou marquée pour.</span><span class="sxs-lookup"><span data-stu-id="f595e-108">[in] The function instance that is being recompiled or marked for recompilation.</span></span> <span data-ttu-id="f595e-109">Cette valeur peut être `NULL` si la défaillance s’est produite sur une base par méthode au lieu d’une base par instanciation (par exemple, si le profileur spécifié un jeton de métadonnées non valide pour la méthode d’être recompilé).</span><span class="sxs-lookup"><span data-stu-id="f595e-109">This value may be `NULL` if the failure occurred on a per-method basis instead of a per-instantiation basis (for example, if the profiler specified an invalid metadata token for the method to be recompiled).</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="f595e-110">[in] HRESULT qui indique la nature de l’échec.</span><span class="sxs-lookup"><span data-stu-id="f595e-110">[in] An HRESULT that indicates the nature of the failure.</span></span> <span data-ttu-id="f595e-111">Consultez la section HRESULT d’état pour obtenir la liste de valeurs.</span><span class="sxs-lookup"><span data-stu-id="f595e-111">See the Status HRESULTS section for a list of values.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f595e-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f595e-112">Return Value</span></span>  
 <span data-ttu-id="f595e-113">Les valeurs retournées depuis ce rappel sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="f595e-113">Return values from this callback are ignored.</span></span>  
  
## <a name="status-hresults"></a><span data-ttu-id="f595e-114">HRESULT d'état</span><span class="sxs-lookup"><span data-stu-id="f595e-114">Status HRESULTS</span></span>  
  
|<span data-ttu-id="f595e-115">HRESULT du tableau d'états</span><span class="sxs-lookup"><span data-stu-id="f595e-115">Status array HRESULT</span></span>|<span data-ttu-id="f595e-116">Description</span><span class="sxs-lookup"><span data-stu-id="f595e-116">Description</span></span>|  
|--------------------------|-----------------|  
|<span data-ttu-id="f595e-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f595e-117">E_INVALIDARG</span></span>|<span data-ttu-id="f595e-118">Le `moduleID` ou `methodDef` jeton est `NULL`.</span><span class="sxs-lookup"><span data-stu-id="f595e-118">The `moduleID` or `methodDef` token is `NULL`.</span></span>|  
|<span data-ttu-id="f595e-119">CORPROF_E_DATAINCOMPLETE</span><span class="sxs-lookup"><span data-stu-id="f595e-119">CORPROF_E_DATAINCOMPLETE</span></span>|<span data-ttu-id="f595e-120">Le module n'est pas encore totalement chargé ou il est en cours de déchargement.</span><span class="sxs-lookup"><span data-stu-id="f595e-120">The module is not fully loaded yet, or it is in the process of being unloaded.</span></span>|  
|<span data-ttu-id="f595e-121">CORPROF_E_MODULE_IS_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="f595e-121">CORPROF_E_MODULE_IS_DYNAMIC</span></span>|<span data-ttu-id="f595e-122">Le module spécifié a été généré dynamiquement (par exemple, en `Reflection.Emit`) et n’est donc pas pris en charge par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f595e-122">The specified module was dynamically generated (for example, by `Reflection.Emit`), and is thus not supported by this method.</span></span>|  
|<span data-ttu-id="f595e-123">CORPROF_E_FUNCTION_IS_COLLECTIBLE</span><span class="sxs-lookup"><span data-stu-id="f595e-123">CORPROF_E_FUNCTION_IS_COLLECTIBLE</span></span>|<span data-ttu-id="f595e-124">La méthode est instanciée dans un assembly pouvant être collecté et n’est donc pas en mesure d’être recompilé.</span><span class="sxs-lookup"><span data-stu-id="f595e-124">The method is instantiated into a collectible assembly, and is therefore not able to be recompiled.</span></span> <span data-ttu-id="f595e-125">Notez que les types et fonctions définies dans un contexte de réflexion non (par exemple, `List<MyCollectibleStruct>`) peut être instancié dans un assembly pouvant être collecté.</span><span class="sxs-lookup"><span data-stu-id="f595e-125">Note that types and functions defined in a non-reflection context (for example, `List<MyCollectibleStruct>`) can be instantiated into a collectible assembly.</span></span>|  
|<span data-ttu-id="f595e-126">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="f595e-126">E_OUTOFMEMORY</span></span>|<span data-ttu-id="f595e-127">Le CLR a manqué de mémoire lors de la tentative de marquer la méthode spécifiée pour la recompilation JIT.</span><span class="sxs-lookup"><span data-stu-id="f595e-127">The CLR ran out of memory while trying to mark the specified method for JIT recompilation.</span></span>|  
|<span data-ttu-id="f595e-128">Autre</span><span class="sxs-lookup"><span data-stu-id="f595e-128">Other</span></span>|<span data-ttu-id="f595e-129">Le système d'exploitation a retourné un échec en dehors du contrôle du CLR.</span><span class="sxs-lookup"><span data-stu-id="f595e-129">The operating system returned a failure outside the control of the CLR.</span></span> <span data-ttu-id="f595e-130">Par exemple, si un appel système pour modifier la protection d’accès d’une page de mémoire échoue, l’erreur de système d’exploitation s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f595e-130">For example, if a system call to change the access protection of a page of memory fails, the operating system error is displayed.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f595e-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f595e-131">Requirements</span></span>  
 <span data-ttu-id="f595e-132">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f595e-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f595e-133">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="f595e-133">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="f595e-134">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f595e-134">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f595e-135">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f595e-135">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f595e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f595e-136">See also</span></span>
- [<span data-ttu-id="f595e-137">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="f595e-137">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="f595e-138">ICorProfilerCallback4, interface</span><span class="sxs-lookup"><span data-stu-id="f595e-138">ICorProfilerCallback4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md)
