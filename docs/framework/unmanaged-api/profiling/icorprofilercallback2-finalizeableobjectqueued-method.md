---
title: ICorProfilerCallback2::FinalizeableObjectQueued, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.FinalizeableObjectQueued
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::FinalizeableObjectQueued
helpviewer_keywords:
- FinalizeableObjectQueued method [.NET Framework profiling]
- ICorProfilerCallback2::FinalizeableObjectQueued method [.NET Framework profiling]
ms.assetid: 92d76893-683c-475d-9996-5bff03cdb10f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e4d10b313adc60e2b851d32aeea70e2993480b0a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33451806"
---
# <a name="icorprofilercallback2finalizeableobjectqueued-method"></a><span data-ttu-id="472af-102">ICorProfilerCallback2::FinalizeableObjectQueued, méthode</span><span class="sxs-lookup"><span data-stu-id="472af-102">ICorProfilerCallback2::FinalizeableObjectQueued Method</span></span>
<span data-ttu-id="472af-103">Notifie le profileur de code à un objet avec un finaliseur a été mis en attente pour le thread finaliseur pour l’exécution de son `Finalize` (méthode).</span><span class="sxs-lookup"><span data-stu-id="472af-103">Notifies the code profiler that an object with a finalizer has been queued to the finalizer thread for execution of its `Finalize` method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="472af-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="472af-104">Syntax</span></span>  
  
```  
HRESULT FinalizeableObjectQueued(  
    [in] DWORD finalizerFlags,  
    [in] ObjectID objectID);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="472af-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="472af-105">Parameters</span></span>  
 `finalizerFlags`  
 <span data-ttu-id="472af-106">[in] Une valeur de la [COR_PRF_FINALIZER_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-finalizer-flags-enumeration.md) énumération qui décrit des aspects du finaliseur.</span><span class="sxs-lookup"><span data-stu-id="472af-106">[in] A value of the [COR_PRF_FINALIZER_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-finalizer-flags-enumeration.md) enumeration that describes aspects of the finalizer.</span></span>  
  
 `objectID`  
 <span data-ttu-id="472af-107">[in] L’ID de l’objet qui a été mis en attente.</span><span class="sxs-lookup"><span data-stu-id="472af-107">[in] The ID of the object that has been queued.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="472af-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="472af-108">Requirements</span></span>  
 <span data-ttu-id="472af-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="472af-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="472af-110">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="472af-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="472af-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="472af-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="472af-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="472af-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="472af-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="472af-113">See Also</span></span>  
 [<span data-ttu-id="472af-114">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="472af-114">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="472af-115">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="472af-115">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
