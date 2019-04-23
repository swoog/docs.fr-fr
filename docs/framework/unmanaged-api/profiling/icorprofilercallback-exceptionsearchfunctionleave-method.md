---
title: ICorProfilerCallback::ExceptionSearchFunctionLeave, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionSearchFunctionLeave
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionSearchFunctionLeave
helpviewer_keywords:
- ExceptionSearchFunctionLeave method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionSearchFunctionLeave method [.NET Framework profiling]
ms.assetid: 01de7ac6-0aad-42ef-bf93-50737667b0a4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bdea3b0cc5b21cd881fe0ff3e0278444a22d083d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59117194"
---
# <a name="icorprofilercallbackexceptionsearchfunctionleave-method"></a><span data-ttu-id="cca5d-102">ICorProfilerCallback::ExceptionSearchFunctionLeave, méthode</span><span class="sxs-lookup"><span data-stu-id="cca5d-102">ICorProfilerCallback::ExceptionSearchFunctionLeave Method</span></span>
<span data-ttu-id="cca5d-103">Notifie le profileur que la phase de recherche de gestion des exceptions a terminé la recherche d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="cca5d-103">Notifies the profiler that the search phase of exception handling has finished searching a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cca5d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cca5d-104">Syntax</span></span>  
  
```  
HRESULT ExceptionSearchFunctionLeave();  
```  
  
## <a name="requirements"></a><span data-ttu-id="cca5d-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cca5d-105">Requirements</span></span>  
 <span data-ttu-id="cca5d-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cca5d-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cca5d-107">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="cca5d-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="cca5d-108">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cca5d-108">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cca5d-109">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cca5d-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cca5d-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cca5d-110">See also</span></span>

- [<span data-ttu-id="cca5d-111">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="cca5d-111">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="cca5d-112">ExceptionSearchFunctionEnter, méthode</span><span class="sxs-lookup"><span data-stu-id="cca5d-112">ExceptionSearchFunctionEnter Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfunctionenter-method.md)
