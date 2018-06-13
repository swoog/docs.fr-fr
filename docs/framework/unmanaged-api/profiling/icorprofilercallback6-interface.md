---
title: ICorProfilerCallback6, interface
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback6
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.assetid: edc420b7-96d1-4dec-ace0-36d907f644bc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 05e571149a794cbffa9e602255455d779a83e2a8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452954"
---
# <a name="icorprofilercallback6-interface"></a><span data-ttu-id="6faac-102">ICorProfilerCallback6, interface</span><span class="sxs-lookup"><span data-stu-id="6faac-102">ICorProfilerCallback6 Interface</span></span>
<span data-ttu-id="6faac-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="6faac-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="6faac-104">Une sous-classe de [ICorProfilerCallback5](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-interface.md) qui fournit une méthode de rappel que le common language runtime utilise pour notifier au profileur que le chargement d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="6faac-104">A subclass of [ICorProfilerCallback5](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-interface.md) that provides a callback method that the common language runtime uses to notify a profiler that an assembly is loading.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6faac-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6faac-105">Methods</span></span>  
  
|<span data-ttu-id="6faac-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="6faac-106">Method</span></span>|<span data-ttu-id="6faac-107">Description</span><span class="sxs-lookup"><span data-stu-id="6faac-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6faac-108">GetAssemblyReferences, méthode</span><span class="sxs-lookup"><span data-stu-id="6faac-108">GetAssemblyReferences Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md)|<span data-ttu-id="6faac-109">Notifie le profileur qu'un assembly en est au tout début du chargement, quand le CLR effectue un parcours de fermeture de références d'assembly.</span><span class="sxs-lookup"><span data-stu-id="6faac-109">Notifies the profiler that an assembly is in a very early loading stage, when the common language runtime performs an assembly reference closure walk.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6faac-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6faac-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6faac-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6faac-111">Requirements</span></span>  
 <span data-ttu-id="6faac-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6faac-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6faac-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="6faac-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="6faac-114">**Versions du .NET framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6faac-114">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6faac-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6faac-115">See Also</span></span>  
 [<span data-ttu-id="6faac-116">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="6faac-116">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
