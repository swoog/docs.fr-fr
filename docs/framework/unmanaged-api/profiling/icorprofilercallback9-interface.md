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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59227754"
---
# <a name="icorprofilercallback9-interface"></a><span data-ttu-id="180eb-102">ICorProfilerCallback9, interface</span><span class="sxs-lookup"><span data-stu-id="180eb-102">ICorProfilerCallback9 Interface</span></span>
<span data-ttu-id="180eb-103">[Pris en charge dans le .NET Framework 4.7.2 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="180eb-103">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  

 <span data-ttu-id="180eb-104">Une sous-classe de [ICorProfilerCallback8](icorprofilercallback8-interface.md) qui fournit une méthode de rappel utilisée par le common language runtime pour informer le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="180eb-104">A subclass of [ICorProfilerCallback8](icorprofilercallback8-interface.md) that provides a callback method used by the common language runtime to notify the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="180eb-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="180eb-105">Methods</span></span>  
  
|<span data-ttu-id="180eb-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="180eb-106">Method</span></span>|<span data-ttu-id="180eb-107">Description</span><span class="sxs-lookup"><span data-stu-id="180eb-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="180eb-108">DynamicMethodUnloaded, méthode</span><span class="sxs-lookup"><span data-stu-id="180eb-108">DynamicMethodUnloaded Method</span></span>](ICorProfilerCallback9-dynamicmethodunloaded-method.md)|<span data-ttu-id="180eb-109">Notifie le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="180eb-109">Notifies the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="180eb-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="180eb-110">Requirements</span></span>  
 <span data-ttu-id="180eb-111">**Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="180eb-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="180eb-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="180eb-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
**<span data-ttu-id="180eb-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="180eb-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  

## <a name="see-also"></a><span data-ttu-id="180eb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="180eb-114">See also</span></span>

- [<span data-ttu-id="180eb-115">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="180eb-115">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="180eb-116">ICorProfilerCallback8, interface</span><span class="sxs-lookup"><span data-stu-id="180eb-116">ICorProfilerCallback8 Interface</span></span>](icorprofilercallback9-interface.md)
- [<span data-ttu-id="180eb-117">ICorProfilerCallback8.DynamicMethodJITCompilationStarted (méthode)</span><span class="sxs-lookup"><span data-stu-id="180eb-117">ICorProfilerCallback8.DynamicMethodJITCompilationStarted method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [<span data-ttu-id="180eb-118">ICorProfilerCallback8.DynamicMethodJITCompilationFinished (méthode)</span><span class="sxs-lookup"><span data-stu-id="180eb-118">ICorProfilerCallback8.DynamicMethodJITCompilationFinished method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
