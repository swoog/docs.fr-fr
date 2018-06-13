---
title: ICorProfilerCallback::FunctionUnloadStarted, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.FunctionUnloadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::FunctionUnloadStarted
helpviewer_keywords:
- FunctionUnloadStarted method [.NET Framework profiling]
- ICorProfilerCallback::FunctionUnloadStarted method [.NET Framework profiling]
ms.assetid: d6a5fa8b-09c6-47a5-b60e-6cf2e355df30
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e28aef4916d06218953236e3b29e19c68822bd6b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33451186"
---
# <a name="icorprofilercallbackfunctionunloadstarted-method"></a><span data-ttu-id="35cdb-102">ICorProfilerCallback::FunctionUnloadStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="35cdb-102">ICorProfilerCallback::FunctionUnloadStarted Method</span></span>
<span data-ttu-id="35cdb-103">Notifie le profileur que le runtime a commencé à décharger une fonction.</span><span class="sxs-lookup"><span data-stu-id="35cdb-103">Notifies the profiler that the runtime has started to unload a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35cdb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35cdb-104">Syntax</span></span>  
  
```  
HRESULT FunctionUnloadStarted(  
    [in] FunctionID functionId);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="35cdb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35cdb-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="35cdb-106">[in] L’ID de la fonction qui est en cours de déchargement.</span><span class="sxs-lookup"><span data-stu-id="35cdb-106">[in] The ID of the function that is being unloaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="35cdb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="35cdb-107">Remarks</span></span>  
 <span data-ttu-id="35cdb-108">La valeur de le `functionId` paramètre n’est plus valide une fois que cette méthode est retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="35cdb-108">The value of the `functionId` parameter is no longer valid after this method returns to the caller.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="35cdb-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="35cdb-109">Requirements</span></span>  
 <span data-ttu-id="35cdb-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="35cdb-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="35cdb-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="35cdb-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="35cdb-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="35cdb-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="35cdb-113">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="35cdb-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="35cdb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35cdb-114">See Also</span></span>  
 [<span data-ttu-id="35cdb-115">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="35cdb-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
