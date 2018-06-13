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
ms.openlocfilehash: beb0e4d3e22ffc3619a6c5281ab5d72efeda921d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33450601"
---
# <a name="icorprofilercallbackexceptionsearchcatcherfound-method"></a><span data-ttu-id="4bc95-102">ICorProfilerCallback::ExceptionSearchCatcherFound, méthode</span><span class="sxs-lookup"><span data-stu-id="4bc95-102">ICorProfilerCallback::ExceptionSearchCatcherFound Method</span></span>
<span data-ttu-id="4bc95-103">Notifie le profileur que la phase de recherche de la gestion des exceptions a trouvé un gestionnaire pour l’exception qui a été levée.</span><span class="sxs-lookup"><span data-stu-id="4bc95-103">Notifies the profiler that the search phase of exception handling has located a handler for the exception that was thrown.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4bc95-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bc95-104">Syntax</span></span>  
  
```  
RESULT ExceptionSearchCatcherFound(  
    [in] FunctionID functionId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4bc95-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bc95-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="4bc95-106">[in] L’ID de la fonction qui contient le Gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="4bc95-106">[in] The ID of the function that contains the exception handler.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4bc95-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4bc95-107">Requirements</span></span>  
 <span data-ttu-id="4bc95-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4bc95-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4bc95-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="4bc95-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="4bc95-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4bc95-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4bc95-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4bc95-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4bc95-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bc95-112">See Also</span></span>  
 [<span data-ttu-id="4bc95-113">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="4bc95-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
