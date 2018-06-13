---
title: ICorProfilerCallback::ClassLoadStarted, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ClassLoadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ClassLoadStarted
helpviewer_keywords:
- ICorProfilerCallback::ClassLoadStarted method [.NET Framework profiling]
- ClassLoadStarted method [.NET Framework profiling]
ms.assetid: 9f728de8-45c2-45a5-ac4a-45660bd36ecf
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: df70041497f000bfd4f6dcac2713e8d5e4eb33f2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33450942"
---
# <a name="icorprofilercallbackclassloadstarted-method"></a><span data-ttu-id="1c89f-102">ICorProfilerCallback::ClassLoadStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="1c89f-102">ICorProfilerCallback::ClassLoadStarted Method</span></span>
<span data-ttu-id="1c89f-103">Notifie le profileur qu’une classe est chargée.</span><span class="sxs-lookup"><span data-stu-id="1c89f-103">Notifies the profiler that a class is being loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1c89f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c89f-104">Syntax</span></span>  
  
```  
HRESULT ClassLoadStarted(  
    [in] ClassID classId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1c89f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c89f-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="1c89f-106">[in] Identifie la classe qui est chargée.</span><span class="sxs-lookup"><span data-stu-id="1c89f-106">[in] Identifies the class that is being loaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1c89f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1c89f-107">Remarks</span></span>  
 <span data-ttu-id="1c89f-108">La valeur de `classId` n’est pas valide pour une demande d’informations jusqu'à ce que le [ICorProfilerCallback::ClassLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classloadfinished-method.md) méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="1c89f-108">The value of `classId` is not valid for an information request until the [ICorProfilerCallback::ClassLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classloadfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1c89f-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1c89f-109">Requirements</span></span>  
 <span data-ttu-id="1c89f-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1c89f-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1c89f-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="1c89f-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="1c89f-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1c89f-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1c89f-113">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1c89f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c89f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c89f-114">See Also</span></span>  
 [<span data-ttu-id="1c89f-115">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="1c89f-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
