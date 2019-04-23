---
title: ICorProfilerCallback7::ModuleInMemorySymbolsUpdated (méthode)
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback7.ModuleInMemorySymbolsUpdated
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.assetid: f362a896-3247-4894-9727-e48dbbcd2c78
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 12414064bf0651eab443951bde2a50dcff7b2291
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59226959"
---
# <a name="icorprofilercallback7moduleinmemorysymbolsupdated-method"></a><span data-ttu-id="51423-102">ICorProfilerCallback7::ModuleInMemorySymbolsUpdated (méthode)</span><span class="sxs-lookup"><span data-stu-id="51423-102">ICorProfilerCallback7::ModuleInMemorySymbolsUpdated Method</span></span>
<span data-ttu-id="51423-103">[Prise en charge dans le .NET Framework 4.6.1 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="51423-103">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="51423-104">Notifie le profileur chaque fois que le flux de symbole associé à un module en mémoire est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="51423-104">Notifies the profiler whenever the symbol stream associated with an in-memory module is updated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="51423-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51423-105">Syntax</span></span>  
  
```  
HRESULT ModuleInMemorySymbolsUpdated(  
     ModuleID moduleId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="51423-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51423-106">Parameters</span></span>  
 <span data-ttu-id="51423-107">[in] `moduleId`</span><span class="sxs-lookup"><span data-stu-id="51423-107">[in] `moduleId`</span></span>  
 <span data-ttu-id="51423-108">L’identificateur du module en mémoire dont flux de symbole est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="51423-108">The identifier of the in-memory module whose symbol stream is updated.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="51423-109">Notes</span><span class="sxs-lookup"><span data-stu-id="51423-109">Remarks</span></span>  
 <span data-ttu-id="51423-110">Ce rappel est contrôlé en définissant le [COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) indicateur de masque d’événement lors de l’appel le [ICorProfilerCallback5::SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="51423-110">This callback is controlled by setting the [COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) event mask flag when calling the [ICorProfilerCallback5::SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="51423-111">Cet événement n’est pas actuellement déclenché pour les symboles implicitement créé ou modifié <xref:System.Reflection.Emit> API.</span><span class="sxs-lookup"><span data-stu-id="51423-111">This event is not currently raised for symbols implicitly created or modified via <xref:System.Reflection.Emit> APIs.</span></span>  
  
 <span data-ttu-id="51423-112">Même lorsque les symboles sont fournis d’en amont dans un appel à une des surcharges de managé <xref:System.Reflection.Assembly.Load*?displayProperty=nameWithType> méthodes qui inclut un `rawSymbolStore` argument pour spécifier les symboles pour l’assembly, le runtime peut associer pas réellement les données symboliques avec le module jusqu'à ce qu’une fois que le [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) rappel s’est produite.</span><span class="sxs-lookup"><span data-stu-id="51423-112">Even when symbols are provided up front in a call to one of the overloads of the managed <xref:System.Reflection.Assembly.Load*?displayProperty=nameWithType> methods that includes a `rawSymbolStore` argument to specify the symbols for the assembly, the runtime may not actually associate the symbolic data with the module until after the [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) callback has occurred.</span></span> <span data-ttu-id="51423-113">Cet événement offre une opportunité ultérieure pour collecter des symboles pour ces modules.</span><span class="sxs-lookup"><span data-stu-id="51423-113">This event provides a later opportunity to collect symbols for such modules.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="51423-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51423-114">Requirements</span></span>  
 <span data-ttu-id="51423-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="51423-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="51423-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="51423-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="51423-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="51423-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="51423-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="51423-118">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51423-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51423-119">See also</span></span>

- [<span data-ttu-id="51423-120">ModuleLoadFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="51423-120">ModuleLoadFinished Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md)
- [<span data-ttu-id="51423-121">SetEventMask2, méthode</span><span class="sxs-lookup"><span data-stu-id="51423-121">SetEventMask2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md)
- [<span data-ttu-id="51423-122">ICorProfilerCallback7, interface</span><span class="sxs-lookup"><span data-stu-id="51423-122">ICorProfilerCallback7 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback7-interface.md)
