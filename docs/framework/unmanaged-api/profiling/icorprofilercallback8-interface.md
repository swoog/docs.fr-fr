---
title: ICorProfilerCallback8 Interface
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback8
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a3bdf79582619777a22c80caac5b4e90d603f3a8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54675013"
---
# <a name="icorprofilercallback8-interface"></a><span data-ttu-id="7fcbe-102">ICorProfilerCallback8 Interface</span><span class="sxs-lookup"><span data-stu-id="7fcbe-102">ICorProfilerCallback8 Interface</span></span>
<span data-ttu-id="7fcbe-103">[Pris en charge dans le .NET Framework 4.7 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="7fcbe-103">[Supported in the .NET Framework 4.7 and later versions]</span></span>  

 <span data-ttu-id="7fcbe-104">Une sous-classe de [ICorProfilerCallback7](icorprofilercallback7-interface.md) qui fournit des méthodes de rappel utilisés par le common language runtime pour informer le profileur de la compilation JIT d’une méthode dynamique a démarré et s’est terminé.</span><span class="sxs-lookup"><span data-stu-id="7fcbe-104">A subclass of [ICorProfilerCallback7](icorprofilercallback7-interface.md) that provides callback methods used by the common language runtime to notify the profiler that JIT compilation of a dynamic method has started and finished.</span></span> 
  
## <a name="methods"></a><span data-ttu-id="7fcbe-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7fcbe-105">Methods</span></span>  
  
|<span data-ttu-id="7fcbe-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="7fcbe-106">Method</span></span>|<span data-ttu-id="7fcbe-107">Description</span><span class="sxs-lookup"><span data-stu-id="7fcbe-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7fcbe-108">DynamicMethodJITCompilationStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="7fcbe-108">DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)|<span data-ttu-id="7fcbe-109">Notifie le profileur que la compilation JIT d’une méthode dynamique a démarré.</span><span class="sxs-lookup"><span data-stu-id="7fcbe-109">Notifies the profiler that JIT compilation of a dynamic method has started.</span></span>|  
|[<span data-ttu-id="7fcbe-110">DynamicMethodJITCompilationFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="7fcbe-110">DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)|<span data-ttu-id="7fcbe-111">Notifie le profileur que la compilation JIT d’une méthode dynamique est terminée.</span><span class="sxs-lookup"><span data-stu-id="7fcbe-111">Notifies the profiler that JIT compilation of a dynamic method has finished.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7fcbe-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7fcbe-112">Requirements</span></span>  
 <span data-ttu-id="7fcbe-113">**Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7fcbe-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7fcbe-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7fcbe-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="7fcbe-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7fcbe-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="7fcbe-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fcbe-116">See also</span></span>
- [<span data-ttu-id="7fcbe-117">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="7fcbe-117">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="7fcbe-118">ICorProfilerCallback9, interface</span><span class="sxs-lookup"><span data-stu-id="7fcbe-118">ICorProfilerCallback9 Interface</span></span>](icorprofilercallback9-interface.md)
