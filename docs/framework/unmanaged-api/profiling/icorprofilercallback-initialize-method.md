---
title: ICorProfilerCallback::Initialize, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.Initialize
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::Initialize
helpviewer_keywords:
- Initialize method, ICorProfilerCallback interface [.NET Framework profiling]
- ICorProfilerCallback::Initialize method [.NET Framework profiling]
ms.assetid: dc5fab2a-4b45-4b12-8727-b89c9915f23e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5aa1025d3f24126c6f8b8585e39dda0201fad3d7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54623311"
---
# <a name="icorprofilercallbackinitialize-method"></a><span data-ttu-id="8055b-102">ICorProfilerCallback::Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="8055b-102">ICorProfilerCallback::Initialize Method</span></span>
<span data-ttu-id="8055b-103">Appelée pour initialiser le profileur de code à chaque démarrage d’une application du common language runtime (CLR) nouvelle.</span><span class="sxs-lookup"><span data-stu-id="8055b-103">Called to initialize the code profiler whenever a new common language runtime (CLR) application is started.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8055b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8055b-104">Syntax</span></span>  
  
```  
HRESULT Initialize(  
    [in] IUnknown     *pICorProfilerInfoUnk);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8055b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8055b-105">Parameters</span></span>  
 `pICorProfilerInfoUnk`  
 <span data-ttu-id="8055b-106">[dans](/cpp/atl/iunknown) interface que le profileur doit interroger pour un [ICorProfilerInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md) pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="8055b-106">[in](/cpp/atl/iunknown) interface that the profiler must query for an [ICorProfilerInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md) interface pointer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8055b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8055b-107">Remarks</span></span>  
 <span data-ttu-id="8055b-108">Le `Initialize` appel est la seule possibilité pour activer (ou désactiver) les rappels qui sont immuables.</span><span class="sxs-lookup"><span data-stu-id="8055b-108">The `Initialize` call is the only opportunity to enable (or disable) callbacks that are immutable.</span></span> <span data-ttu-id="8055b-109">Une fois qu’un rappel est activé par le `Initialize` appeler, il ne peut pas être désactivée ultérieurement à l’aide [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md).</span><span class="sxs-lookup"><span data-stu-id="8055b-109">Once a callback is enabled by the `Initialize` call, it cannot be disabled later using [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md).</span></span> <span data-ttu-id="8055b-110">La valeur COR_PRF_MONITOR_IMMUTABLE de le [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) énumération indique les événements qui sont immuables.</span><span class="sxs-lookup"><span data-stu-id="8055b-110">The COR_PRF_MONITOR_IMMUTABLE value of the [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumeration indicates which events are immutable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8055b-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8055b-111">Requirements</span></span>  
 <span data-ttu-id="8055b-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8055b-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8055b-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8055b-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8055b-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8055b-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8055b-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8055b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8055b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8055b-116">See also</span></span>
- [<span data-ttu-id="8055b-117">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="8055b-117">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="8055b-118">Shutdown, méthode</span><span class="sxs-lookup"><span data-stu-id="8055b-118">Shutdown Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-shutdown-method.md)
