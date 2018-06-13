---
title: ICorProfilerCallback2::HandleCreated, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.HandleCreated
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::HandleCreated
helpviewer_keywords:
- HandleCreated method [.NET Framework profiling]
- ICorProfilerCallback2::HandleCreated method [.NET Framework profiling]
ms.assetid: 6bbb7786-7c38-490f-9834-91aa2795c355
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 47654d7ad1803e57f5db846ea0370d1f736deaa5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452271"
---
# <a name="icorprofilercallback2handlecreated-method"></a><span data-ttu-id="8ec64-102">ICorProfilerCallback2::HandleCreated, méthode</span><span class="sxs-lookup"><span data-stu-id="8ec64-102">ICorProfilerCallback2::HandleCreated Method</span></span>
<span data-ttu-id="8ec64-103">Notifie le profileur de code qu’un handle de garbage collection a été créé.</span><span class="sxs-lookup"><span data-stu-id="8ec64-103">Notifies the code profiler that a garbage collection handle has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ec64-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ec64-104">Syntax</span></span>  
  
```  
HRESULT HandleCreated(  
    [in] GCHandleID handleId,  
    [in] ObjectID initialObjectId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8ec64-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ec64-105">Parameters</span></span>  
 `handleId`  
 <span data-ttu-id="8ec64-106">[in] ID du handle pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="8ec64-106">[in] The ID of the handle for the garbage collection.</span></span>  
  
 `initialObjectId`  
 <span data-ttu-id="8ec64-107">[in] L’ID de l’objet pour lequel le handle de garbage collection a été créé.</span><span class="sxs-lookup"><span data-stu-id="8ec64-107">[in] The ID of the object for which the garbage collection handle was created.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ec64-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8ec64-108">Requirements</span></span>  
 <span data-ttu-id="8ec64-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8ec64-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ec64-110">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8ec64-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8ec64-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8ec64-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8ec64-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ec64-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ec64-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ec64-113">See Also</span></span>  
 [<span data-ttu-id="8ec64-114">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="8ec64-114">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="8ec64-115">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="8ec64-115">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
