---
title: ICorProfilerCallback::ClassUnloadStarted, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ClassUnloadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ClassUnloadStarted
helpviewer_keywords:
- ClassUnloadStarted method [.NET Framework profiling]
- ICorProfilerCallback::ClassUnloadStarted method [.NET Framework profiling]
ms.assetid: bc93bead-f3a9-415c-b919-ddd3ca80facc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2c30fb5d5576a7bed403f48504ead923df212de9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33450373"
---
# <a name="icorprofilercallbackclassunloadstarted-method"></a><span data-ttu-id="242f8-102">ICorProfilerCallback::ClassUnloadStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="242f8-102">ICorProfilerCallback::ClassUnloadStarted Method</span></span>
<span data-ttu-id="242f8-103">Notifie le profileur qu’une classe est en cours de déchargement.</span><span class="sxs-lookup"><span data-stu-id="242f8-103">Notifies the profiler that a class is being unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="242f8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="242f8-104">Syntax</span></span>  
  
```  
HRESULT ClassUnloadStarted(  
    [in] ClassID classId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="242f8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="242f8-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="242f8-106">[in] Identifie la classe qui est en cours de déchargement.</span><span class="sxs-lookup"><span data-stu-id="242f8-106">[in] Identifies the class that is being unloaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="242f8-107">Notes</span><span class="sxs-lookup"><span data-stu-id="242f8-107">Remarks</span></span>  
 <span data-ttu-id="242f8-108">La valeur de `classId` n’est pas valide pour une demande d’informations après le `ClassUnloadStarted` retours de méthode, il s’agit permet du profileur d’obtenir des informations sur cette classe.</span><span class="sxs-lookup"><span data-stu-id="242f8-108">The value of `classId` is not valid for an information request after the `ClassUnloadStarted` method returns — this is the profiler's last chance to obtain information about this class.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="242f8-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="242f8-109">Requirements</span></span>  
 <span data-ttu-id="242f8-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="242f8-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="242f8-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="242f8-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="242f8-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="242f8-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="242f8-113">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="242f8-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="242f8-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="242f8-114">See Also</span></span>  
 [<span data-ttu-id="242f8-115">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="242f8-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="242f8-116">ClassUnloadFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="242f8-116">ClassUnloadFinished Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classunloadfinished-method.md)
