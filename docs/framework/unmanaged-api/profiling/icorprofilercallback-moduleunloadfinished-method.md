---
title: ICorProfilerCallback::ModuleUnloadFinished, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleUnloadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleUnloadFinished
helpviewer_keywords:
- ModuleUnloadFinished method [.NET Framework profiling]
- ICorProfilerCallback::ModuleUnloadFinished method [.NET Framework profiling]
ms.assetid: 185e3327-9f9c-44bc-8a5c-febea9a6bb5b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6462fe44459228a377f4e583a8a5a1cd93d939bb
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57480362"
---
# <a name="icorprofilercallbackmoduleunloadfinished-method"></a><span data-ttu-id="0190e-102">ICorProfilerCallback::ModuleUnloadFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="0190e-102">ICorProfilerCallback::ModuleUnloadFinished Method</span></span>
<span data-ttu-id="0190e-103">Notifie le profileur qu’un module a été déchargé.</span><span class="sxs-lookup"><span data-stu-id="0190e-103">Notifies the profiler that a module has finished unloading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0190e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0190e-104">Syntax</span></span>  
  
```  
HRESULT ModuleUnloadFinished(  
    [in] ModuleID moduleId,  
    [in] HRESULT  hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0190e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0190e-105">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="0190e-106">[in] L’ID du module qui a été déchargé.</span><span class="sxs-lookup"><span data-stu-id="0190e-106">[in] The ID of the module that was unloaded.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="0190e-107">[in] HRESULT qui indique si le module a été déchargé.</span><span class="sxs-lookup"><span data-stu-id="0190e-107">[in] An HRESULT that indicates whether the module was unloaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0190e-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0190e-108">Remarks</span></span>  
 <span data-ttu-id="0190e-109">La valeur de `moduleId` n’est pas valide pour une demande d’informations après la [ICorProfilerCallback::ModuleUnloadStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleunloadstarted-method.md) méthode retourne.</span><span class="sxs-lookup"><span data-stu-id="0190e-109">The value of `moduleId` is not valid for an information request after the [ICorProfilerCallback::ModuleUnloadStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleunloadstarted-method.md) method returns.</span></span>  
  
 <span data-ttu-id="0190e-110">Certaines parties du déchargement de la classe peuvent continuer après le `ModuleUnloadFinished` rappel.</span><span class="sxs-lookup"><span data-stu-id="0190e-110">Some parts of unloading the class might continue after the `ModuleUnloadFinished` callback.</span></span> <span data-ttu-id="0190e-111">Un HRESULT d’échec dans `hrStatus` indique un échec.</span><span class="sxs-lookup"><span data-stu-id="0190e-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="0190e-112">Toutefois, un HRESULT de réussite dans `hrStatus` indique uniquement que la première partie du déchargement du module a réussi.</span><span class="sxs-lookup"><span data-stu-id="0190e-112">However, a success HRESULT in `hrStatus` indicates only that the first part of unloading the module has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0190e-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0190e-113">Requirements</span></span>  
 <span data-ttu-id="0190e-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0190e-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0190e-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="0190e-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="0190e-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0190e-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0190e-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0190e-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0190e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0190e-118">See also</span></span>
- [<span data-ttu-id="0190e-119">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="0190e-119">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
