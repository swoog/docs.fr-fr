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
ms.openlocfilehash: 27e68c82a04b78a18f51f0a2c9ec712036521368
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54513540"
---
# <a name="icorprofilercallback9dynamicmethodunloaded-method"></a><span data-ttu-id="06552-102">ICorProfilerCallback9::DynamicMethodUnloaded (méthode)</span><span class="sxs-lookup"><span data-stu-id="06552-102">ICorProfilerCallback9::DynamicMethodUnloaded Method</span></span>
<span data-ttu-id="06552-103">[Pris en charge dans le .NET Framework 4.7.2 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="06552-103">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  
  
<span data-ttu-id="06552-104">Notifie le profileur chaque fois qu’une méthode dynamique est garbage collectées et déchargé par la suite.</span><span class="sxs-lookup"><span data-stu-id="06552-104">Notifies the profiler whenever a dynamic method is garbage collected and subsequently unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06552-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06552-105">Syntax</span></span>  
  
```  
HRESULT DynamicMethodUnloaded(  
     [in]  FunctionID  functionId
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="06552-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06552-106">Parameters</span></span>  
<span data-ttu-id="06552-107">[in] `functionId`</span><span class="sxs-lookup"><span data-stu-id="06552-107">[in] `functionId`</span></span>  
<span data-ttu-id="06552-108">L’identificateur de la fonction en mémoire qui a été garbage collectées et déchargé.</span><span class="sxs-lookup"><span data-stu-id="06552-108">The identifier of the in-memory function that has been garbage collected and unloaded.</span></span>   

## <a name="requirements"></a><span data-ttu-id="06552-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="06552-109">Requirements</span></span>  
 <span data-ttu-id="06552-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="06552-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="06552-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="06552-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="06552-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="06552-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="06552-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="06552-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06552-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06552-114">See also</span></span>
- [<span data-ttu-id="06552-115">ICorProfilerCallback8.DynamicMethodJITCompilationStarted (méthode)</span><span class="sxs-lookup"><span data-stu-id="06552-115">ICorProfilerCallback8.DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [<span data-ttu-id="06552-116">ICorProfilerCallback8.DynamicMethodJITCompilationFinished (méthode)</span><span class="sxs-lookup"><span data-stu-id="06552-116">ICorProfilerCallback8.DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
- [<span data-ttu-id="06552-117">ICorProfilerCallback9, interface</span><span class="sxs-lookup"><span data-stu-id="06552-117">ICorProfilerCallback9 Interface</span></span>](icorprofilercallback9-interface.md)
- [<span data-ttu-id="06552-118">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span><span class="sxs-lookup"><span data-stu-id="06552-118">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span></span>](cor-prf-high-monitor-enumeration.md)
