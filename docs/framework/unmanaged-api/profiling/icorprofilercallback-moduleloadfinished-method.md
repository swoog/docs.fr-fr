---
title: ICorProfilerCallback::ModuleLoadFinished, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleLoadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleLoadFinished
helpviewer_keywords:
- ModuleLoadFinished method [.NET Framework profiling]
- ICorProfilerCallback::ModuleLoadFinished method [.NET Framework profiling]
ms.assetid: 050649e5-ffc0-4458-a0a4-d9ee128a219e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 14f918a312031359043076be0b739f9b7e0e9f2a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33451641"
---
# <a name="icorprofilercallbackmoduleloadfinished-method"></a><span data-ttu-id="fe492-102">ICorProfilerCallback::ModuleLoadFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="fe492-102">ICorProfilerCallback::ModuleLoadFinished Method</span></span>
<span data-ttu-id="fe492-103">Notifie le profileur qu’un module a été chargé.</span><span class="sxs-lookup"><span data-stu-id="fe492-103">Notifies the profiler that a module has finished loading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe492-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe492-104">Syntax</span></span>  
  
```  
HRESULT ModuleLoadFinished(  
    [in] ModuleID moduleId,  
    [in] HRESULT  hrStatus);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fe492-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe492-105">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="fe492-106">[in] L’ID du module qui a terminé son chargement.</span><span class="sxs-lookup"><span data-stu-id="fe492-106">[in] The ID of the module that has finished loading.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="fe492-107">[in] HRESULT qui indique si le module a été chargé avec succès.</span><span class="sxs-lookup"><span data-stu-id="fe492-107">[in] An HRESULT that indicates whether the module was loaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fe492-108">Notes</span><span class="sxs-lookup"><span data-stu-id="fe492-108">Remarks</span></span>  
 <span data-ttu-id="fe492-109">La valeur de `moduleId` n’est pas valide pour une demande d’informations jusqu'à ce que le `ModuleLoadFinished` méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="fe492-109">The value of `moduleId` is not valid for an information request until the `ModuleLoadFinished` method is called.</span></span>  
  
 <span data-ttu-id="fe492-110">Certaines parties du chargement du module peuvent continuer après le `ModuleLoadFinished` rappel.</span><span class="sxs-lookup"><span data-stu-id="fe492-110">Some parts of loading the module might continue after the `ModuleLoadFinished` callback.</span></span> <span data-ttu-id="fe492-111">Un HRESULT d’échec dans `hrStatus` indique un échec.</span><span class="sxs-lookup"><span data-stu-id="fe492-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="fe492-112">Toutefois, un HRESULT de réussite dans `hrStatus` indique uniquement que la première partie du chargement du module a réussi.</span><span class="sxs-lookup"><span data-stu-id="fe492-112">However, a success HRESULT in `hrStatus` indicates only that the first part of loading the module has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe492-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe492-113">Requirements</span></span>  
 <span data-ttu-id="fe492-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fe492-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe492-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fe492-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fe492-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fe492-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fe492-117">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe492-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe492-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe492-118">See Also</span></span>  
 [<span data-ttu-id="fe492-119">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="fe492-119">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="fe492-120">ModuleLoadStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="fe492-120">ModuleLoadStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadstarted-method.md)
