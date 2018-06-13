---
title: ICorProfilerCallback2::ThreadNameChanged, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.ThreadNameChanged
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::ThreadNameChanged
helpviewer_keywords:
- ThreadNameChanged method [.NET Framework profiling]
- ICorProfilerCallback2::ThreadNameChanged method [.NET Framework profiling]
ms.assetid: c8bbd76d-a9ff-44f2-87a6-be052819da36
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6bf11d71b90f11a5d9a3844ed59a8574b7b76699
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452570"
---
# <a name="icorprofilercallback2threadnamechanged-method"></a><span data-ttu-id="348c8-102">ICorProfilerCallback2::ThreadNameChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="348c8-102">ICorProfilerCallback2::ThreadNameChanged Method</span></span>
<span data-ttu-id="348c8-103">Notifie le profileur de code que le nom d’un thread a changé.</span><span class="sxs-lookup"><span data-stu-id="348c8-103">Notifies the code profiler that the name of a thread has changed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="348c8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="348c8-104">Syntax</span></span>  
  
```  
HRESULT ThreadNameChanged(  
    [in] ThreadID threadId,  
    [in] ULONG cchName,  
    [in] WCHAR name[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="348c8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="348c8-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="348c8-106">[in] L’ID du thread.</span><span class="sxs-lookup"><span data-stu-id="348c8-106">[in] The ID of the thread.</span></span>  
  
 `cchName`  
 <span data-ttu-id="348c8-107">[in] La longueur du nouveau nom du thread.</span><span class="sxs-lookup"><span data-stu-id="348c8-107">[in] The length of the new name of the thread.</span></span>  
  
 `name`  
 <span data-ttu-id="348c8-108">[in] Le nouveau nom du thread.</span><span class="sxs-lookup"><span data-stu-id="348c8-108">[in] The new name of the thread.</span></span> <span data-ttu-id="348c8-109">Le nom ne se termine pas par une valeur null.</span><span class="sxs-lookup"><span data-stu-id="348c8-109">The name is not null-terminated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="348c8-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="348c8-110">Requirements</span></span>  
 <span data-ttu-id="348c8-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="348c8-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="348c8-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="348c8-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="348c8-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="348c8-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="348c8-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="348c8-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="348c8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="348c8-115">See Also</span></span>  
 [<span data-ttu-id="348c8-116">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="348c8-116">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="348c8-117">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="348c8-117">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
