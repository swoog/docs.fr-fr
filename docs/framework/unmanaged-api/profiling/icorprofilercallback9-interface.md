---
title: Interface de ICorProfilerCallback9
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
ms.openlocfilehash: 488af069e7798fde650abb1473df256eed2d692f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452375"
---
# <a name="icorprofilercallback9-interface"></a><span data-ttu-id="1bce6-102">Interface de ICorProfilerCallback9</span><span class="sxs-lookup"><span data-stu-id="1bce6-102">ICorProfilerCallback9 Interface</span></span>
<span data-ttu-id="1bce6-103">[Pris en charge dans le .NET Framework 4.7.2 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="1bce6-103">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  

 <span data-ttu-id="1bce6-104">Une sous-classe de [ICorProfilerCallback8](icorprofilercallback8-interface.md) qui fournit une méthode de rappel utilisée par le common language runtime pour informer le profileur qu’une méthode dynamique a été garbage collector et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="1bce6-104">A subclass of [ICorProfilerCallback8](icorprofilercallback8-interface.md) that provides a callback method used by the common language runtime to notify the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1bce6-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1bce6-105">Methods</span></span>  
  
|<span data-ttu-id="1bce6-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="1bce6-106">Method</span></span>|<span data-ttu-id="1bce6-107">Description</span><span class="sxs-lookup"><span data-stu-id="1bce6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1bce6-108">DynamicMethodUnloaded (méthode)</span><span class="sxs-lookup"><span data-stu-id="1bce6-108">DynamicMethodUnloaded Method</span></span>](ICorProfilerCallback9-dynamicmethodunloaded-method.md)|<span data-ttu-id="1bce6-109">Notifie le profileur qu’une méthode dynamique a été garbage collector et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="1bce6-109">Notifies the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1bce6-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1bce6-110">Requirements</span></span>  
 <span data-ttu-id="1bce6-111">**Plateformes :** consultez [requise](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1bce6-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1bce6-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="1bce6-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="1bce6-113">**Versions du .NET framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="1bce6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="1bce6-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bce6-114">See Also</span></span>  
<span data-ttu-id="1bce6-115">[Interfaces de profilage](profiling-interfaces.md) </span><span class="sxs-lookup"><span data-stu-id="1bce6-115">[Profiling Interfaces](profiling-interfaces.md) </span></span>  
<span data-ttu-id="1bce6-116">[Interface de ICorProfilerCallback8](icorprofilercallback9-interface.md) </span><span class="sxs-lookup"><span data-stu-id="1bce6-116">[ICorProfilerCallback8 Interface](icorprofilercallback9-interface.md) </span></span>  
<span data-ttu-id="1bce6-117">[ICorProfilerCallback8.DynamicMethodJITCompilationStarted (méthode)](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md) </span><span class="sxs-lookup"><span data-stu-id="1bce6-117">[ICorProfilerCallback8.DynamicMethodJITCompilationStarted method](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md) </span></span>  
[<span data-ttu-id="1bce6-118">ICorProfilerCallback8.DynamicMethodJITCompilationFinished (méthode)</span><span class="sxs-lookup"><span data-stu-id="1bce6-118">ICorProfilerCallback8.DynamicMethodJITCompilationFinished method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)   
