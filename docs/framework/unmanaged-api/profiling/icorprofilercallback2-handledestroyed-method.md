---
title: ICorProfilerCallback2::HandleDestroyed, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.HandleDestroyed
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::HandleDestroyed
helpviewer_keywords:
- ICorProfilerCallback2::HandleDestroyed method [.NET Framework profiling]
- HandleDestroyed method [.NET Framework profiling]
ms.assetid: ab4f4bbd-40c7-4667-bfde-60cd73803110
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 31492711ea9927c07f611ff9ec9bbe49d4857d46
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33451959"
---
# <a name="icorprofilercallback2handledestroyed-method"></a><span data-ttu-id="b909e-102">ICorProfilerCallback2::HandleDestroyed, méthode</span><span class="sxs-lookup"><span data-stu-id="b909e-102">ICorProfilerCallback2::HandleDestroyed Method</span></span>
<span data-ttu-id="b909e-103">Notifie le profileur de code qu’un handle de garbage collection a été détruit.</span><span class="sxs-lookup"><span data-stu-id="b909e-103">Notifies the code profiler that a garbage collection handle has been destroyed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b909e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b909e-104">Syntax</span></span>  
  
```  
HRESULT HandleDestroyed(  
    [in] GCHandleID handleId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b909e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b909e-105">Parameters</span></span>  
 `handleId`  
 <span data-ttu-id="b909e-106">[in] ID du handle pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="b909e-106">[in] The ID of the handle for the garbage collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b909e-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b909e-107">Requirements</span></span>  
 <span data-ttu-id="b909e-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b909e-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b909e-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b909e-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b909e-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b909e-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b909e-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b909e-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b909e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b909e-112">See Also</span></span>  
 [<span data-ttu-id="b909e-113">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="b909e-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="b909e-114">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="b909e-114">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
