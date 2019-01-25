---
title: ICorProfilerInfo::GetThreadContext, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetThreadContext
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetThreadContext
helpviewer_keywords:
- ICorProfilerInfo::GetThreadContext method [.NET Framework profiling]
- GetThreadContext method, ICorProfilerInfo interface [.NET Framework profiling]
ms.assetid: 79446216-4b8b-484c-8fe3-e87dbf9df2fd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cb686be625d0d38bcf0de496c192276ebaa3410d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629568"
---
# <a name="icorprofilerinfogetthreadcontext-method"></a><span data-ttu-id="8dcac-102">ICorProfilerInfo::GetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="8dcac-102">ICorProfilerInfo::GetThreadContext Method</span></span>
<span data-ttu-id="8dcac-103">Obtient l’identité de contexte actuellement associée au thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="8dcac-103">Gets the context identity currently associated with the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8dcac-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8dcac-104">Syntax</span></span>  
  
```  
HRESULT GetThreadContext(  
    [in]  ThreadID  threadId,  
    [out] ContextID *pContextId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8dcac-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8dcac-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="8dcac-106">[in] L’ID du thread.</span><span class="sxs-lookup"><span data-stu-id="8dcac-106">[in] The ID of the thread.</span></span>  
  
 `pContextId`  
 <span data-ttu-id="8dcac-107">[out] Pointeur vers l’ID de contexte actuellement associé au thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="8dcac-107">[out] A pointer to the context ID currently associated with the specified thread.</span></span> <span data-ttu-id="8dcac-108">Si le thread a aucun contexte actuellement associé, cette fonction retournera CORPROF_E_DATAINCOMPLETE.</span><span class="sxs-lookup"><span data-stu-id="8dcac-108">If the thread has no context currently associated with it, this function will return CORPROF_E_DATAINCOMPLETE.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8dcac-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8dcac-109">Requirements</span></span>  
 <span data-ttu-id="8dcac-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8dcac-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8dcac-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8dcac-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8dcac-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8dcac-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8dcac-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8dcac-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8dcac-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dcac-114">See also</span></span>
- [<span data-ttu-id="8dcac-115">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="8dcac-115">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
