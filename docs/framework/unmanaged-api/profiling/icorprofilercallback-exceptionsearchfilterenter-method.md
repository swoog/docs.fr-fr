---
title: ICorProfilerCallback::ExceptionSearchFilterEnter, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionSearchFilterEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionSearchFilterEnter
helpviewer_keywords:
- ExceptionSearchFilterEnter method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionSearchFilterEnter method [.NET Framework profiling]
ms.assetid: acc239ce-3eef-418c-b1df-c5a6dd8e8a4c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 08ac7eddf96ac54ce16696355f7d5bb5694f872b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33450981"
---
# <a name="icorprofilercallbackexceptionsearchfilterenter-method"></a><span data-ttu-id="de10c-102">ICorProfilerCallback::ExceptionSearchFilterEnter, méthode</span><span class="sxs-lookup"><span data-stu-id="de10c-102">ICorProfilerCallback::ExceptionSearchFilterEnter Method</span></span>
<span data-ttu-id="de10c-103">Notifie le profileur que la phase de recherche de la gestion des exceptions a commencé l’exécution d’un filtre d’exception définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="de10c-103">Notifies the profiler that the search phase of exception handling has begun executing a user-defined exception filter.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de10c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de10c-104">Syntax</span></span>  
  
```  
HRESULT ExceptionSearchFilterEnter(  
    [in] FunctionID functionId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="de10c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de10c-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="de10c-106">[in] L’ID de la fonction qui contient le filtre.</span><span class="sxs-lookup"><span data-stu-id="de10c-106">[in] The ID of the function that contains the filter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="de10c-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="de10c-107">Requirements</span></span>  
 <span data-ttu-id="de10c-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="de10c-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="de10c-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="de10c-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="de10c-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="de10c-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="de10c-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="de10c-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de10c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de10c-112">See Also</span></span>  
 [<span data-ttu-id="de10c-113">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="de10c-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="de10c-114">ExceptionSearchFilterLeave, méthode</span><span class="sxs-lookup"><span data-stu-id="de10c-114">ExceptionSearchFilterLeave Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfilterleave-method.md)
