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
ms.openlocfilehash: dbd9374decdce171d45e57512470c652abc24882
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59173668"
---
# <a name="icorprofilercallback2threadnamechanged-method"></a><span data-ttu-id="0d80d-102">ICorProfilerCallback2::ThreadNameChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="0d80d-102">ICorProfilerCallback2::ThreadNameChanged Method</span></span>
<span data-ttu-id="0d80d-103">Notifie le profileur de code que le nom d’un thread a changé.</span><span class="sxs-lookup"><span data-stu-id="0d80d-103">Notifies the code profiler that the name of a thread has changed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0d80d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d80d-104">Syntax</span></span>  
  
```  
HRESULT ThreadNameChanged(  
    [in] ThreadID threadId,  
    [in] ULONG cchName,  
    [in] WCHAR name[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0d80d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d80d-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="0d80d-106">[in] L’ID du thread.</span><span class="sxs-lookup"><span data-stu-id="0d80d-106">[in] The ID of the thread.</span></span>  
  
 `cchName`  
 <span data-ttu-id="0d80d-107">[in] La longueur du nouveau nom du thread.</span><span class="sxs-lookup"><span data-stu-id="0d80d-107">[in] The length of the new name of the thread.</span></span>  
  
 `name`  
 <span data-ttu-id="0d80d-108">[in] Le nouveau nom du thread.</span><span class="sxs-lookup"><span data-stu-id="0d80d-108">[in] The new name of the thread.</span></span> <span data-ttu-id="0d80d-109">Le nom ne se termine pas par une valeur null.</span><span class="sxs-lookup"><span data-stu-id="0d80d-109">The name is not null-terminated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0d80d-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d80d-110">Requirements</span></span>  
 <span data-ttu-id="0d80d-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0d80d-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0d80d-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="0d80d-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="0d80d-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0d80d-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="0d80d-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0d80d-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0d80d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d80d-115">See also</span></span>

- [<span data-ttu-id="0d80d-116">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="0d80d-116">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="0d80d-117">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="0d80d-117">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
