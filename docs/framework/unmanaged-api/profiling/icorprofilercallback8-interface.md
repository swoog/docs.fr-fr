---
title: Interface de ICorProfilerCallback8
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
ms.openlocfilehash: b92120cc5948efca696d922448da215601f9e6b3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455281"
---
# <a name="icorprofilercallback8-interface"></a><span data-ttu-id="98857-102">Interface de ICorProfilerCallback8</span><span class="sxs-lookup"><span data-stu-id="98857-102">ICorProfilerCallback8 Interface</span></span>
<span data-ttu-id="98857-103">[Pris en charge dans le .NET Framework 4.7 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="98857-103">[Supported in the .NET Framework 4.7 and later versions]</span></span>  

 <span data-ttu-id="98857-104">Une sous-classe de [ICorProfilerCallback7](icorprofilercallback7-interface.md) qui fournit des méthodes de rappel utilisés par le common language runtime pour informer le profileur de la compilation JIT d’une méthode dynamique a démarré et s’est terminé.</span><span class="sxs-lookup"><span data-stu-id="98857-104">A subclass of [ICorProfilerCallback7](icorprofilercallback7-interface.md) that provides callback methods used by the common language runtime to notify the profiler that JIT compilation of a dynamic method has started and finished.</span></span> 
  
## <a name="methods"></a><span data-ttu-id="98857-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="98857-105">Methods</span></span>  
  
|<span data-ttu-id="98857-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="98857-106">Method</span></span>|<span data-ttu-id="98857-107">Description</span><span class="sxs-lookup"><span data-stu-id="98857-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="98857-108">DynamicMethodJITCompilationStarted (méthode)</span><span class="sxs-lookup"><span data-stu-id="98857-108">DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)|<span data-ttu-id="98857-109">Notifie le profileur que la compilation JIT d’une méthode dynamique a démarré.</span><span class="sxs-lookup"><span data-stu-id="98857-109">Notifies the profiler that JIT compilation of a dynamic method has started.</span></span>|  
|[<span data-ttu-id="98857-110">DynamicMethodJITCompilationFinished (méthode)</span><span class="sxs-lookup"><span data-stu-id="98857-110">DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)|<span data-ttu-id="98857-111">Notifie le profileur que la compilation JIT d’une méthode dynamique est terminée.</span><span class="sxs-lookup"><span data-stu-id="98857-111">Notifies the profiler that JIT compilation of a dynamic method has finished.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="98857-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="98857-112">Requirements</span></span>  
 <span data-ttu-id="98857-113">**Plateformes :** consultez [requise](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="98857-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="98857-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="98857-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="98857-115">**Versions du .NET framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="98857-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="98857-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98857-116">See Also</span></span>  
<span data-ttu-id="98857-117">[Interfaces de profilage](profiling-interfaces.md) </span><span class="sxs-lookup"><span data-stu-id="98857-117">[Profiling Interfaces](profiling-interfaces.md) </span></span>  
[<span data-ttu-id="98857-118">Interface de ICorProfilerCallback9</span><span class="sxs-lookup"><span data-stu-id="98857-118">ICorProfilerCallback9 Interface</span></span>](icorprofilercallback9-interface.md)
