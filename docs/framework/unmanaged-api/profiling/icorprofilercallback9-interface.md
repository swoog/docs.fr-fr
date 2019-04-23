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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59227754"
---
# <a name="icorprofilercallback9-interface"></a><span data-ttu-id="afcbc-102">ICorProfilerCallback9, interface</span><span class="sxs-lookup"><span data-stu-id="afcbc-102">ICorProfilerCallback9 Interface</span></span>
<span data-ttu-id="afcbc-103">[Pris en charge dans le .NET Framework 4.7.2 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="afcbc-103">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  

 <span data-ttu-id="afcbc-104">Une sous-classe de [ICorProfilerCallback8](icorprofilercallback8-interface.md) qui fournit une méthode de rappel utilisée par le common language runtime pour informer le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="afcbc-104">A subclass of [ICorProfilerCallback8](icorprofilercallback8-interface.md) that provides a callback method used by the common language runtime to notify the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="afcbc-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="afcbc-105">Methods</span></span>  
  
|<span data-ttu-id="afcbc-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="afcbc-106">Method</span></span>|<span data-ttu-id="afcbc-107">Description</span><span class="sxs-lookup"><span data-stu-id="afcbc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="afcbc-108">DynamicMethodUnloaded, méthode</span><span class="sxs-lookup"><span data-stu-id="afcbc-108">DynamicMethodUnloaded Method</span></span>](ICorProfilerCallback9-dynamicmethodunloaded-method.md)|<span data-ttu-id="afcbc-109">Notifie le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="afcbc-109">Notifies the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="afcbc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afcbc-110">Requirements</span></span>  
 <span data-ttu-id="afcbc-111">**Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="afcbc-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="afcbc-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="afcbc-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="afcbc-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="afcbc-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="afcbc-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afcbc-114">See also</span></span>

- [<span data-ttu-id="afcbc-115">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="afcbc-115">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="afcbc-116">ICorProfilerCallback8, interface</span><span class="sxs-lookup"><span data-stu-id="afcbc-116">ICorProfilerCallback8 Interface</span></span>](icorprofilercallback9-interface.md)
- [<span data-ttu-id="afcbc-117">ICorProfilerCallback8.DynamicMethodJITCompilationStarted (méthode)</span><span class="sxs-lookup"><span data-stu-id="afcbc-117">ICorProfilerCallback8.DynamicMethodJITCompilationStarted method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [<span data-ttu-id="afcbc-118">ICorProfilerCallback8.DynamicMethodJITCompilationFinished (méthode)</span><span class="sxs-lookup"><span data-stu-id="afcbc-118">ICorProfilerCallback8.DynamicMethodJITCompilationFinished method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
