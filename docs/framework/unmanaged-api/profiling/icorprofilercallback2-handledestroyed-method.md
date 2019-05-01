---
title: ICorProfilerCallback2::HandleDestroyed, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.HandleDestroyed
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::HandleDestroyed
helpviewer_keywords:
- ICorProfilerCallback2::HandleDestroyed method [.NET Framework profiling]
- HandleDestroyed method [.NET Framework profiling]
ms.assetid: ab4f4bbd-40c7-4667-bfde-60cd73803110
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bc6b086b444a769afbf01369b50c69e242a21050
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62041559"
---
# <a name="icorprofilercallback2handledestroyed-method"></a><span data-ttu-id="a5043-102">ICorProfilerCallback2::HandleDestroyed, méthode</span><span class="sxs-lookup"><span data-stu-id="a5043-102">ICorProfilerCallback2::HandleDestroyed Method</span></span>
<span data-ttu-id="a5043-103">Notifie le profileur de code qu’un handle de garbage collection a été détruit.</span><span class="sxs-lookup"><span data-stu-id="a5043-103">Notifies the code profiler that a garbage collection handle has been destroyed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a5043-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5043-104">Syntax</span></span>  
  
```  
HRESULT HandleDestroyed(  
    [in] GCHandleID handleId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a5043-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5043-105">Parameters</span></span>  
 `handleId`  
 <span data-ttu-id="a5043-106">[in] L’ID du handle pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="a5043-106">[in] The ID of the handle for the garbage collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a5043-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5043-107">Requirements</span></span>  
 <span data-ttu-id="a5043-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a5043-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a5043-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a5043-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a5043-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a5043-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a5043-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a5043-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a5043-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5043-112">See also</span></span>

- [<span data-ttu-id="a5043-113">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="a5043-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="a5043-114">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="a5043-114">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
