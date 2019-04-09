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
ms.openlocfilehash: db7a033944272756a739dec39d4df11fde1d48b3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59178605"
---
# <a name="icorprofilercallbackclassloadstarted-method"></a><span data-ttu-id="97785-102">ICorProfilerCallback::ClassLoadStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="97785-102">ICorProfilerCallback::ClassLoadStarted Method</span></span>
<span data-ttu-id="97785-103">Informe le profileur qu’une classe est chargée.</span><span class="sxs-lookup"><span data-stu-id="97785-103">Notifies the profiler that a class is being loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97785-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97785-104">Syntax</span></span>  
  
```  
HRESULT ClassLoadStarted(  
    [in] ClassID classId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="97785-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97785-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="97785-106">[in] Identifie la classe qui est en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="97785-106">[in] Identifies the class that is being loaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="97785-107">Notes</span><span class="sxs-lookup"><span data-stu-id="97785-107">Remarks</span></span>  
 <span data-ttu-id="97785-108">La valeur de `classId` n’est pas valide pour une demande d’informations jusqu'à ce que le [ICorProfilerCallback::ClassLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classloadfinished-method.md) méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="97785-108">The value of `classId` is not valid for an information request until the [ICorProfilerCallback::ClassLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classloadfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="97785-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97785-109">Requirements</span></span>  
 <span data-ttu-id="97785-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="97785-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="97785-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="97785-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="97785-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="97785-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="97785-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="97785-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="97785-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97785-114">See also</span></span>

- [<span data-ttu-id="97785-115">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="97785-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
