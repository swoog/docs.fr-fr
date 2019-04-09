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
ms.openlocfilehash: 9d01f3d7485b19c076d9cd3e83aeccbcf5e728f4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59160704"
---
# <a name="icorprofilercallbackclassunloadfinished-method"></a><span data-ttu-id="0a59a-102">ICorProfilerCallback::ClassUnloadFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="0a59a-102">ICorProfilerCallback::ClassUnloadFinished Method</span></span>
<span data-ttu-id="0a59a-103">Notifie le profileur qu’une classe a été déchargée.</span><span class="sxs-lookup"><span data-stu-id="0a59a-103">Notifies the profiler that a class has finished unloading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a59a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a59a-104">Syntax</span></span>  
  
```  
HRESULT ClassUnloadFinished(  
    [in] ClassID classId,  
    [in] HRESULT hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0a59a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a59a-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="0a59a-106">[in] Identifie la classe qui a été déchargée.</span><span class="sxs-lookup"><span data-stu-id="0a59a-106">[in] Identifies the class that was unloaded.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="0a59a-107">[in] HRESULT qui indique si la classe a été déchargée.</span><span class="sxs-lookup"><span data-stu-id="0a59a-107">[in] An HRESULT that indicates whether the class was unloaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0a59a-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0a59a-108">Remarks</span></span>  
 <span data-ttu-id="0a59a-109">Certaines parties du déchargement de la classe peuvent continuer après le `ClassUnloadFinished` rappel.</span><span class="sxs-lookup"><span data-stu-id="0a59a-109">Some parts of unloading the class might continue after the `ClassUnloadFinished` callback.</span></span> <span data-ttu-id="0a59a-110">Un HRESULT d’échec dans `hrStatus` indique un échec.</span><span class="sxs-lookup"><span data-stu-id="0a59a-110">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="0a59a-111">Toutefois, un HRESULT de réussite dans `hrStatus` indique uniquement que la première partie du déchargement de la classe a réussi.</span><span class="sxs-lookup"><span data-stu-id="0a59a-111">However, a success HRESULT in `hrStatus` indicates only that the first part of unloading the class has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0a59a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a59a-112">Requirements</span></span>  
 <span data-ttu-id="0a59a-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0a59a-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0a59a-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="0a59a-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="0a59a-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0a59a-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="0a59a-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0a59a-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0a59a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a59a-117">See also</span></span>

- [<span data-ttu-id="0a59a-118">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="0a59a-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="0a59a-119">ClassUnloadStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="0a59a-119">ClassUnloadStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classunloadstarted-method.md)
