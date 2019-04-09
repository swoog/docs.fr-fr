---
title: Interface ICorProfilerCallback7
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback7
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.assetid: a0be019e-aaa1-4036-990f-565f114d4b5c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 81477010b22edee71098edfc1b8557db08b6038f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59178631"
---
# <a name="icorprofilercallback7-interface"></a><span data-ttu-id="73429-102">Interface ICorProfilerCallback7</span><span class="sxs-lookup"><span data-stu-id="73429-102">ICorProfilerCallback7 Interface</span></span>
<span data-ttu-id="73429-103">[Prise en charge dans le .NET Framework 4.6.1 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="73429-103">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="73429-104">Sous-classe de [ICorProfilerCallback6](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-interface.md) qui fournit une méthode de rappel que le Common Language Runtime utilise pour informer le profileur de la mise à jour du flux de symbole associé à un module en mémoire.</span><span class="sxs-lookup"><span data-stu-id="73429-104">A subclass of [ICorProfilerCallback6](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-interface.md) that provides a callback method that the common language runtime uses to notify the profiler that the symbol stream associated with an in-memory module is updated.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="73429-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="73429-105">Methods</span></span>  
  
|<span data-ttu-id="73429-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="73429-106">Method</span></span>|<span data-ttu-id="73429-107">Description</span><span class="sxs-lookup"><span data-stu-id="73429-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="73429-108">ModuleInMemorySymbolsUpdated, méthode</span><span class="sxs-lookup"><span data-stu-id="73429-108">ModuleInMemorySymbolsUpdated Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback7-moduleinmemorysymbolsupdated-method.md)|<span data-ttu-id="73429-109">Notifie le profileur de la mise à jour du flux de symbole associé à un module en mémoire.</span><span class="sxs-lookup"><span data-stu-id="73429-109">Notifies the profiler that the symbol stream associated with an in-memory module is updated.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="73429-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73429-110">Requirements</span></span>  
 <span data-ttu-id="73429-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="73429-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="73429-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="73429-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 **<span data-ttu-id="73429-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="73429-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="73429-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73429-114">See also</span></span>

- [<span data-ttu-id="73429-115">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="73429-115">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
