---
title: ICorProfilerCallback9 Interface
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback9
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a6c480af921fb0259ef85beec8d8f65bdd430522
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689308"
---
# <a name="icorprofilercallback9-interface"></a><span data-ttu-id="d6d9e-102">ICorProfilerCallback9 Interface</span><span class="sxs-lookup"><span data-stu-id="d6d9e-102">ICorProfilerCallback9 Interface</span></span>
<span data-ttu-id="d6d9e-103">[Pris en charge dans le .NET Framework 4.7.2 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="d6d9e-103">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  

 <span data-ttu-id="d6d9e-104">Une sous-classe de [ICorProfilerCallback8](icorprofilercallback8-interface.md) qui fournit une méthode de rappel utilisée par le common language runtime pour informer le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="d6d9e-104">A subclass of [ICorProfilerCallback8](icorprofilercallback8-interface.md) that provides a callback method used by the common language runtime to notify the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d6d9e-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d6d9e-105">Methods</span></span>  
  
|<span data-ttu-id="d6d9e-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="d6d9e-106">Method</span></span>|<span data-ttu-id="d6d9e-107">Description</span><span class="sxs-lookup"><span data-stu-id="d6d9e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d6d9e-108">DynamicMethodUnloaded, méthode</span><span class="sxs-lookup"><span data-stu-id="d6d9e-108">DynamicMethodUnloaded Method</span></span>](ICorProfilerCallback9-dynamicmethodunloaded-method.md)|<span data-ttu-id="d6d9e-109">Notifie le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="d6d9e-109">Notifies the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d6d9e-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d6d9e-110">Requirements</span></span>  
 <span data-ttu-id="d6d9e-111">**Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d6d9e-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d6d9e-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d6d9e-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="d6d9e-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d6d9e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="d6d9e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6d9e-114">See also</span></span>
- [<span data-ttu-id="d6d9e-115">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="d6d9e-115">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="d6d9e-116">ICorProfilerCallback8, interface</span><span class="sxs-lookup"><span data-stu-id="d6d9e-116">ICorProfilerCallback8 Interface</span></span>](icorprofilercallback9-interface.md)
- [<span data-ttu-id="d6d9e-117">ICorProfilerCallback8.DynamicMethodJITCompilationStarted (méthode)</span><span class="sxs-lookup"><span data-stu-id="d6d9e-117">ICorProfilerCallback8.DynamicMethodJITCompilationStarted method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [<span data-ttu-id="d6d9e-118">ICorProfilerCallback8.DynamicMethodJITCompilationFinished (méthode)</span><span class="sxs-lookup"><span data-stu-id="d6d9e-118">ICorProfilerCallback8.DynamicMethodJITCompilationFinished method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
