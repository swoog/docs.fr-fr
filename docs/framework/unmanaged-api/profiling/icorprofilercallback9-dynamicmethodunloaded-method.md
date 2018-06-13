---
title: ICorProfilerCallback9::DynamicMethodUnloaded (méthode)
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback9.DynamicMethodUnloaded
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 16b3334647922f845645e6eb58db3146f4c9b936
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452401"
---
# <a name="icorprofilercallback9dynamicmethodunloaded-method"></a><span data-ttu-id="2f7c0-102">ICorProfilerCallback9::DynamicMethodUnloaded (méthode)</span><span class="sxs-lookup"><span data-stu-id="2f7c0-102">ICorProfilerCallback9::DynamicMethodUnloaded Method</span></span>
<span data-ttu-id="2f7c0-103">[Pris en charge dans le .NET Framework 4.7.2 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="2f7c0-103">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  
  
<span data-ttu-id="2f7c0-104">Notifie le profileur chaque fois qu’une méthode dynamique est garbage collector et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="2f7c0-104">Notifies the profiler whenever a dynamic method is garbage collected and subsequently unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f7c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f7c0-105">Syntax</span></span>  
  
```  
HRESULT DynamicMethodUnloaded(  
     [in]  FunctionID  functionId
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2f7c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f7c0-106">Parameters</span></span>  
<span data-ttu-id="2f7c0-107">[in] `functionId`</span><span class="sxs-lookup"><span data-stu-id="2f7c0-107">[in] `functionId`</span></span>  
<span data-ttu-id="2f7c0-108">Identificateur de la fonction en mémoire qui a été garbage collector et de déchargement.</span><span class="sxs-lookup"><span data-stu-id="2f7c0-108">The identifier of the in-memory function that has been garbage collected and unloaded.</span></span>   

## <a name="requirements"></a><span data-ttu-id="2f7c0-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2f7c0-109">Requirements</span></span>  
 <span data-ttu-id="2f7c0-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2f7c0-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2f7c0-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2f7c0-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2f7c0-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2f7c0-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2f7c0-113">**Versions du .NET framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="2f7c0-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f7c0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f7c0-114">See Also</span></span>  
[<span data-ttu-id="2f7c0-115">ICorProfilerCallback8.DynamicMethodJITCompilationStarted (méthode)</span><span class="sxs-lookup"><span data-stu-id="2f7c0-115">ICorProfilerCallback8.DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)  
[<span data-ttu-id="2f7c0-116">ICorProfilerCallback8.DynamicMethodJITCompilationFinished (méthode)</span><span class="sxs-lookup"><span data-stu-id="2f7c0-116">ICorProfilerCallback8.DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)  
<span data-ttu-id="2f7c0-117">[Interface de ICorProfilerCallback9](icorprofilercallback9-interface.md) </span><span class="sxs-lookup"><span data-stu-id="2f7c0-117">[ICorProfilerCallback9 Interface](icorprofilercallback9-interface.md) </span></span>  
[<span data-ttu-id="2f7c0-118">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span><span class="sxs-lookup"><span data-stu-id="2f7c0-118">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span></span>](cor-prf-high-monitor-enumeration.md)
