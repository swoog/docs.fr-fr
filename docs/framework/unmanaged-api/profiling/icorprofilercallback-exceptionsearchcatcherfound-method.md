---
title: ICorProfilerCallback::ExceptionSearchCatcherFound, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionSearchCatcherFound
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionSearchCatcherFound
helpviewer_keywords:
- ExceptionSearchCatcherFound method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionSearchCatcherFound method [.NET Framework profiling]
ms.assetid: 190f424d-5e37-4163-a191-0895686e9476
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a4dc6b66aff34bae869737591040e5fc1e552834
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57499665"
---
# <a name="icorprofilercallbackexceptionsearchcatcherfound-method"></a><span data-ttu-id="034eb-102">ICorProfilerCallback::ExceptionSearchCatcherFound, méthode</span><span class="sxs-lookup"><span data-stu-id="034eb-102">ICorProfilerCallback::ExceptionSearchCatcherFound Method</span></span>
<span data-ttu-id="034eb-103">Notifie le profileur que la phase de recherche de gestion des exceptions a trouvé un gestionnaire pour l’exception qui a été levée.</span><span class="sxs-lookup"><span data-stu-id="034eb-103">Notifies the profiler that the search phase of exception handling has located a handler for the exception that was thrown.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="034eb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="034eb-104">Syntax</span></span>  
  
```  
RESULT ExceptionSearchCatcherFound(  
    [in] FunctionID functionId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="034eb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="034eb-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="034eb-106">[in] ID de la fonction qui contient le Gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="034eb-106">[in] The ID of the function that contains the exception handler.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="034eb-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="034eb-107">Requirements</span></span>  
 <span data-ttu-id="034eb-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="034eb-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="034eb-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="034eb-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="034eb-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="034eb-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="034eb-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="034eb-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="034eb-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="034eb-112">See also</span></span>
- [<span data-ttu-id="034eb-113">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="034eb-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
