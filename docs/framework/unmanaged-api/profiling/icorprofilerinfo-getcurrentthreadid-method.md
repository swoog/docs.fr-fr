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
ms.openlocfilehash: 89f7ff2c213dc510268f9e6c802813a48e870d99
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33453846"
---
# <a name="icorprofilerinfogetcurrentthreadid-method"></a><span data-ttu-id="c233e-102">ICorProfilerInfo::GetCurrentThreadID, méthode</span><span class="sxs-lookup"><span data-stu-id="c233e-102">ICorProfilerInfo::GetCurrentThreadID Method</span></span>
<span data-ttu-id="c233e-103">Obtient l’ID du thread actuel, s’il s’agit d’un thread managé.</span><span class="sxs-lookup"><span data-stu-id="c233e-103">Gets the ID of the current thread, if it is a managed thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c233e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c233e-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentThreadID(  
    [out] ThreadID *pThreadId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c233e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c233e-105">Parameters</span></span>  
 `pThreadId`  
 <span data-ttu-id="c233e-106">[out] Pointeur vers l’ID retourné du thread managé.</span><span class="sxs-lookup"><span data-stu-id="c233e-106">[out] A pointer to the returned ID of the managed thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c233e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c233e-107">Remarks</span></span>  
 <span data-ttu-id="c233e-108">Si le thread actuel est un thread d’exécution interne ou un autre thread non managé, `GetCurrentThreadID` retourne CORPROF_E_NOT_MANAGED_THREAD comme HRESULT et la valeur retournée de la `pThreadId` paramètre sera null.</span><span class="sxs-lookup"><span data-stu-id="c233e-108">If the current thread is an internal runtime thread or other unmanaged thread, `GetCurrentThreadID` returns CORPROF_E_NOT_MANAGED_THREAD as the HRESULT, and the returned value of the `pThreadId` parameter will be null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c233e-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c233e-109">Requirements</span></span>  
 <span data-ttu-id="c233e-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c233e-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c233e-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c233e-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c233e-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c233e-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c233e-113">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c233e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c233e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c233e-114">See Also</span></span>  
 [<span data-ttu-id="c233e-115">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="c233e-115">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
