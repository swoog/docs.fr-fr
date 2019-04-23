---
title: ICorProfilerCallback8, interface
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
ms.openlocfilehash: e536e61a8d812e442e1e54188c99d6a1d4586757
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59125565"
---
# <a name="icorprofilercallback8-interface"></a><span data-ttu-id="fc5c6-102">ICorProfilerCallback8, interface</span><span class="sxs-lookup"><span data-stu-id="fc5c6-102">ICorProfilerCallback8 Interface</span></span>
<span data-ttu-id="fc5c6-103">[Pris en charge dans le .NET Framework 4.7 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="fc5c6-103">[Supported in the .NET Framework 4.7 and later versions]</span></span>  

 <span data-ttu-id="fc5c6-104">Une sous-classe de [ICorProfilerCallback7](icorprofilercallback7-interface.md) qui fournit des méthodes de rappel utilisés par le common language runtime pour informer le profileur de la compilation JIT d’une méthode dynamique a démarré et s’est terminé.</span><span class="sxs-lookup"><span data-stu-id="fc5c6-104">A subclass of [ICorProfilerCallback7](icorprofilercallback7-interface.md) that provides callback methods used by the common language runtime to notify the profiler that JIT compilation of a dynamic method has started and finished.</span></span> 
  
## <a name="methods"></a><span data-ttu-id="fc5c6-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fc5c6-105">Methods</span></span>  
  
|<span data-ttu-id="fc5c6-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="fc5c6-106">Method</span></span>|<span data-ttu-id="fc5c6-107">Description</span><span class="sxs-lookup"><span data-stu-id="fc5c6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fc5c6-108">DynamicMethodJITCompilationStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="fc5c6-108">DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)|<span data-ttu-id="fc5c6-109">Notifie le profileur que la compilation JIT d’une méthode dynamique a démarré.</span><span class="sxs-lookup"><span data-stu-id="fc5c6-109">Notifies the profiler that JIT compilation of a dynamic method has started.</span></span>|  
|[<span data-ttu-id="fc5c6-110">DynamicMethodJITCompilationFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="fc5c6-110">DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)|<span data-ttu-id="fc5c6-111">Notifie le profileur que la compilation JIT d’une méthode dynamique est terminée.</span><span class="sxs-lookup"><span data-stu-id="fc5c6-111">Notifies the profiler that JIT compilation of a dynamic method has finished.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fc5c6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc5c6-112">Requirements</span></span>  
 <span data-ttu-id="fc5c6-113">**Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fc5c6-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fc5c6-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fc5c6-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="fc5c6-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="fc5c6-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="fc5c6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc5c6-116">See also</span></span>

- [<span data-ttu-id="fc5c6-117">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="fc5c6-117">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="fc5c6-118">ICorProfilerCallback9, interface</span><span class="sxs-lookup"><span data-stu-id="fc5c6-118">ICorProfilerCallback9 Interface</span></span>](icorprofilercallback9-interface.md)
