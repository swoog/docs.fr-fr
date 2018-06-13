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
ms.openlocfilehash: 9658ad8a1963d3747fb7c23dce84790a30b17db3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33453220"
---
# <a name="icorprofilerinfogethandlefromthread-method"></a><span data-ttu-id="9a2ae-102">ICorProfilerInfo::GetHandleFromThread, méthode</span><span class="sxs-lookup"><span data-stu-id="9a2ae-102">ICorProfilerInfo::GetHandleFromThread Method</span></span>
<span data-ttu-id="9a2ae-103">Mappe l’ID d’un thread à un handle de thread Win32.</span><span class="sxs-lookup"><span data-stu-id="9a2ae-103">Maps the ID of a thread to a Win32 thread handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a2ae-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a2ae-104">Syntax</span></span>  
  
```  
HRESULT GetHandleFromThread(  
    [in]  ThreadID threadId,  
    [out] HANDLE  *phThread);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9a2ae-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a2ae-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="9a2ae-106">[in] L’ID de thread à mapper.</span><span class="sxs-lookup"><span data-stu-id="9a2ae-106">[in] The thread ID to be mapped.</span></span>  
  
 `phThread`  
 <span data-ttu-id="9a2ae-107">[out] Pointeur vers un handle de thread Win32.</span><span class="sxs-lookup"><span data-stu-id="9a2ae-107">[out] A pointer to a Win32 thread handle.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9a2ae-108">Notes</span><span class="sxs-lookup"><span data-stu-id="9a2ae-108">Remarks</span></span>  
 <span data-ttu-id="9a2ae-109">Le profileur doit appeler Win32 `DuplicateHandle` fonction sur le handle avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="9a2ae-109">The profiler must call the Win32 `DuplicateHandle` function on the handle before using it.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9a2ae-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9a2ae-110">Requirements</span></span>  
 <span data-ttu-id="9a2ae-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9a2ae-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9a2ae-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="9a2ae-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="9a2ae-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9a2ae-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9a2ae-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9a2ae-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a2ae-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a2ae-115">See Also</span></span>  
 [<span data-ttu-id="9a2ae-116">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="9a2ae-116">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
