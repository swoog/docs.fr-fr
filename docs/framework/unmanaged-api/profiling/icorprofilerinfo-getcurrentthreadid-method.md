---
title: ICorProfilerInfo::GetCurrentThreadID, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetCurrentThreadID
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetCurrentThreadID
helpviewer_keywords:
- GetCurrentThreadID method, ICorProfilerInfo interface [.NET Framework profiling]
- ICorProfilerInfo::GetCurrentThreadID method [.NET Framework profiling]
ms.assetid: 39bbdb30-6a7a-4202-8da3-67ae9a0ab3a8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8be698d27ce69f955e5c1f17f5258602880c4021
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54618696"
---
# <a name="icorprofilerinfogetcurrentthreadid-method"></a><span data-ttu-id="fa4b7-102">ICorProfilerInfo::GetCurrentThreadID, méthode</span><span class="sxs-lookup"><span data-stu-id="fa4b7-102">ICorProfilerInfo::GetCurrentThreadID Method</span></span>
<span data-ttu-id="fa4b7-103">Obtient l’ID du thread actuel, s’il s’agit d’un thread managé.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-103">Gets the ID of the current thread, if it is a managed thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa4b7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa4b7-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentThreadID(  
    [out] ThreadID *pThreadId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fa4b7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa4b7-105">Parameters</span></span>  
 `pThreadId`  
 <span data-ttu-id="fa4b7-106">[out] Pointeur vers l’ID retourné du thread managé.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-106">[out] A pointer to the returned ID of the managed thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fa4b7-107">Notes</span><span class="sxs-lookup"><span data-stu-id="fa4b7-107">Remarks</span></span>  
 <span data-ttu-id="fa4b7-108">Si le thread actuel est un thread d’exécution interne ou un autre thread non managé, `GetCurrentThreadID` retourne CORPROF_E_NOT_MANAGED_THREAD comme HRESULT et la valeur retournée de la `pThreadId` paramètre sera null.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-108">If the current thread is an internal runtime thread or other unmanaged thread, `GetCurrentThreadID` returns CORPROF_E_NOT_MANAGED_THREAD as the HRESULT, and the returned value of the `pThreadId` parameter will be null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fa4b7-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fa4b7-109">Requirements</span></span>  
 <span data-ttu-id="fa4b7-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fa4b7-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa4b7-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fa4b7-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fa4b7-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fa4b7-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fa4b7-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa4b7-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa4b7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa4b7-114">See also</span></span>
- [<span data-ttu-id="fa4b7-115">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="fa4b7-115">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
