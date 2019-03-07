---
title: ICorProfilerInfo::GetHandleFromThread, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetHandleFromThread
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetHandleFromThread
helpviewer_keywords:
- GetHandleFromThread method [.NET Framework profiling]
- ICorProfilerInfo::GetHandleFromThread method [.NET Framework profiling]
ms.assetid: 36cdc9f5-7579-4cd2-aa36-fc05c741584c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ad9dc185514bfddd15a6110b1b0d80fc99230271
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57472276"
---
# <a name="icorprofilerinfogethandlefromthread-method"></a><span data-ttu-id="3b396-102">ICorProfilerInfo::GetHandleFromThread, méthode</span><span class="sxs-lookup"><span data-stu-id="3b396-102">ICorProfilerInfo::GetHandleFromThread Method</span></span>
<span data-ttu-id="3b396-103">Mappe l’ID d’un thread à un handle de thread Win32.</span><span class="sxs-lookup"><span data-stu-id="3b396-103">Maps the ID of a thread to a Win32 thread handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b396-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b396-104">Syntax</span></span>  
  
```  
HRESULT GetHandleFromThread(  
    [in]  ThreadID threadId,  
    [out] HANDLE  *phThread);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3b396-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b396-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="3b396-106">[in] L’ID de thread à mapper.</span><span class="sxs-lookup"><span data-stu-id="3b396-106">[in] The thread ID to be mapped.</span></span>  
  
 `phThread`  
 <span data-ttu-id="3b396-107">[out] Un pointeur vers un handle de thread Win32.</span><span class="sxs-lookup"><span data-stu-id="3b396-107">[out] A pointer to a Win32 thread handle.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3b396-108">Notes</span><span class="sxs-lookup"><span data-stu-id="3b396-108">Remarks</span></span>  
 <span data-ttu-id="3b396-109">Le profileur doit appeler Win32 `DuplicateHandle` fonction sur le handle avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="3b396-109">The profiler must call the Win32 `DuplicateHandle` function on the handle before using it.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b396-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3b396-110">Requirements</span></span>  
 <span data-ttu-id="3b396-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3b396-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3b396-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3b396-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3b396-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3b396-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3b396-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3b396-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b396-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b396-115">See also</span></span>
- [<span data-ttu-id="3b396-116">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="3b396-116">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
