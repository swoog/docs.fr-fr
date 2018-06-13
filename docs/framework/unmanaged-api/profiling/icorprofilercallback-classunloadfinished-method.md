---
title: ICorProfilerCallback::ClassUnloadFinished, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ClassUnloadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ClassUnloadFinished
helpviewer_keywords:
- ICorProfilerCallback::ClassUnloadFinished method [.NET Framework profiling]
- ClassUnloadFinished method [.NET Framework profiling]
ms.assetid: 55674b68-678a-4747-ae06-4e91519c7305
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ebf72fe4f9fae5b3d791e6eed2e9421b9f4e3296
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33450815"
---
# <a name="icorprofilercallbackclassunloadfinished-method"></a><span data-ttu-id="afbd7-102">ICorProfilerCallback::ClassUnloadFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="afbd7-102">ICorProfilerCallback::ClassUnloadFinished Method</span></span>
<span data-ttu-id="afbd7-103">Notifie le profileur qu’une classe a été déchargée.</span><span class="sxs-lookup"><span data-stu-id="afbd7-103">Notifies the profiler that a class has finished unloading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="afbd7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afbd7-104">Syntax</span></span>  
  
```  
HRESULT ClassUnloadFinished(  
    [in] ClassID classId,  
    [in] HRESULT hrStatus);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="afbd7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="afbd7-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="afbd7-106">[in] Identifie la classe qui a été déchargée.</span><span class="sxs-lookup"><span data-stu-id="afbd7-106">[in] Identifies the class that was unloaded.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="afbd7-107">[in] HRESULT qui indique si la classe a été déchargée.</span><span class="sxs-lookup"><span data-stu-id="afbd7-107">[in] An HRESULT that indicates whether the class was unloaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="afbd7-108">Notes</span><span class="sxs-lookup"><span data-stu-id="afbd7-108">Remarks</span></span>  
 <span data-ttu-id="afbd7-109">Certaines parties du déchargement de la classe peuvent continuer après le `ClassUnloadFinished` rappel.</span><span class="sxs-lookup"><span data-stu-id="afbd7-109">Some parts of unloading the class might continue after the `ClassUnloadFinished` callback.</span></span> <span data-ttu-id="afbd7-110">Un HRESULT d’échec dans `hrStatus` indique un échec.</span><span class="sxs-lookup"><span data-stu-id="afbd7-110">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="afbd7-111">Toutefois, un HRESULT de réussite dans `hrStatus` indique uniquement que la première partie du déchargement de la classe a réussi.</span><span class="sxs-lookup"><span data-stu-id="afbd7-111">However, a success HRESULT in `hrStatus` indicates only that the first part of unloading the class has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="afbd7-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="afbd7-112">Requirements</span></span>  
 <span data-ttu-id="afbd7-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="afbd7-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="afbd7-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="afbd7-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="afbd7-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="afbd7-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="afbd7-116">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="afbd7-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="afbd7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afbd7-117">See Also</span></span>  
 [<span data-ttu-id="afbd7-118">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="afbd7-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="afbd7-119">ClassUnloadStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="afbd7-119">ClassUnloadStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classunloadstarted-method.md)
