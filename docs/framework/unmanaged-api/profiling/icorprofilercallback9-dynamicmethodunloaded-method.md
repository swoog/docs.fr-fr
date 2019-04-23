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
ms.openlocfilehash: 96cdfb79c1573648173305d6ee789aa8db030ff8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59211008"
---
# <a name="icorprofilercallback9dynamicmethodunloaded-method"></a><span data-ttu-id="dbf57-102">ICorProfilerCallback9::DynamicMethodUnloaded (méthode)</span><span class="sxs-lookup"><span data-stu-id="dbf57-102">ICorProfilerCallback9::DynamicMethodUnloaded Method</span></span>
<span data-ttu-id="dbf57-103">[Pris en charge dans le .NET Framework 4.7.2 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="dbf57-103">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  
  
<span data-ttu-id="dbf57-104">Notifie le profileur chaque fois qu’une méthode dynamique est garbage collectées et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="dbf57-104">Notifies the profiler whenever a dynamic method is garbage collected and subsequently unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dbf57-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbf57-105">Syntax</span></span>  
  
```  
HRESULT DynamicMethodUnloaded(  
     [in]  FunctionID  functionId
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dbf57-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbf57-106">Parameters</span></span>  
<span data-ttu-id="dbf57-107">[in] `functionId`</span><span class="sxs-lookup"><span data-stu-id="dbf57-107">[in] `functionId`</span></span>  
<span data-ttu-id="dbf57-108">L’identificateur de la fonction en mémoire qui a été garbage collectées et déchargé.</span><span class="sxs-lookup"><span data-stu-id="dbf57-108">The identifier of the in-memory function that has been garbage collected and unloaded.</span></span>   

## <a name="requirements"></a><span data-ttu-id="dbf57-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbf57-109">Requirements</span></span>  
 <span data-ttu-id="dbf57-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dbf57-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dbf57-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="dbf57-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="dbf57-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dbf57-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dbf57-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="dbf57-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dbf57-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbf57-114">See also</span></span>

- [<span data-ttu-id="dbf57-115">ICorProfilerCallback8.DynamicMethodJITCompilationStarted (méthode)</span><span class="sxs-lookup"><span data-stu-id="dbf57-115">ICorProfilerCallback8.DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [<span data-ttu-id="dbf57-116">ICorProfilerCallback8.DynamicMethodJITCompilationFinished (méthode)</span><span class="sxs-lookup"><span data-stu-id="dbf57-116">ICorProfilerCallback8.DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
- [<span data-ttu-id="dbf57-117">ICorProfilerCallback9, interface</span><span class="sxs-lookup"><span data-stu-id="dbf57-117">ICorProfilerCallback9 Interface</span></span>](icorprofilercallback9-interface.md)
- [<span data-ttu-id="dbf57-118">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span><span class="sxs-lookup"><span data-stu-id="dbf57-118">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span></span>](cor-prf-high-monitor-enumeration.md)
