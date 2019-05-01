---
title: ICorProfilerCallback9, interface
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
ms.openlocfilehash: e1711def5e2aa41fd63912361ef8250ad160fb88
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61991989"
---
# <a name="icorprofilercallback9-interface"></a><span data-ttu-id="2dbe7-102">ICorProfilerCallback9, interface</span><span class="sxs-lookup"><span data-stu-id="2dbe7-102">ICorProfilerCallback9 Interface</span></span>
<span data-ttu-id="2dbe7-103">[Pris en charge dans le .NET Framework 4.7.2 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="2dbe7-103">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  

 <span data-ttu-id="2dbe7-104">Une sous-classe de [ICorProfilerCallback8](icorprofilercallback8-interface.md) qui fournit une méthode de rappel utilisée par le common language runtime pour informer le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="2dbe7-104">A subclass of [ICorProfilerCallback8](icorprofilercallback8-interface.md) that provides a callback method used by the common language runtime to notify the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2dbe7-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2dbe7-105">Methods</span></span>  
  
|<span data-ttu-id="2dbe7-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="2dbe7-106">Method</span></span>|<span data-ttu-id="2dbe7-107">Description</span><span class="sxs-lookup"><span data-stu-id="2dbe7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2dbe7-108">DynamicMethodUnloaded, méthode</span><span class="sxs-lookup"><span data-stu-id="2dbe7-108">DynamicMethodUnloaded Method</span></span>](ICorProfilerCallback9-dynamicmethodunloaded-method.md)|<span data-ttu-id="2dbe7-109">Notifie le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="2dbe7-109">Notifies the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2dbe7-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2dbe7-110">Requirements</span></span>  
 <span data-ttu-id="2dbe7-111">**Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2dbe7-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2dbe7-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2dbe7-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="2dbe7-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="2dbe7-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="2dbe7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2dbe7-114">See also</span></span>

- [<span data-ttu-id="2dbe7-115">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="2dbe7-115">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="2dbe7-116">ICorProfilerCallback8, interface</span><span class="sxs-lookup"><span data-stu-id="2dbe7-116">ICorProfilerCallback8 Interface</span></span>](icorprofilercallback9-interface.md)
- [<span data-ttu-id="2dbe7-117">ICorProfilerCallback8.DynamicMethodJITCompilationStarted (méthode)</span><span class="sxs-lookup"><span data-stu-id="2dbe7-117">ICorProfilerCallback8.DynamicMethodJITCompilationStarted method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [<span data-ttu-id="2dbe7-118">ICorProfilerCallback8.DynamicMethodJITCompilationFinished (méthode)</span><span class="sxs-lookup"><span data-stu-id="2dbe7-118">ICorProfilerCallback8.DynamicMethodJITCompilationFinished method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
