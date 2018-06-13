---
title: ICorProfilerInfo5, interface
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo5
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: 7bd48c34-37ed-4230-9eec-39a17280f05d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4ba082182ec7e2f639ef94baeb29203ee792fba0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455326"
---
# <a name="icorprofilerinfo5-interface"></a><span data-ttu-id="4a500-102">ICorProfilerInfo5, interface</span><span class="sxs-lookup"><span data-stu-id="4a500-102">ICorProfilerInfo5 Interface</span></span>
<span data-ttu-id="4a500-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="4a500-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="4a500-104">Une sous-classe de [ICorProfilerInfo4](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md) qui fournit des méthodes pour une utilisation par les profileurs de code pour communiquer avec le common language runtime (CLR) pour contrôler la surveillance de l’événement.</span><span class="sxs-lookup"><span data-stu-id="4a500-104">A subclass of [ICorProfilerInfo4](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md) that provides methods for use by code profilers to communicate with the common language runtime (CLR) to control event monitoring.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4a500-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4a500-105">Methods</span></span>  
  
|<span data-ttu-id="4a500-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="4a500-106">Method</span></span>|<span data-ttu-id="4a500-107">Description</span><span class="sxs-lookup"><span data-stu-id="4a500-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4a500-108">GetEventMask2, méthode</span><span class="sxs-lookup"><span data-stu-id="4a500-108">GetEventMask2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-geteventmask2-method.md)|<span data-ttu-id="4a500-109">Obtient les catégories des événements actifs pour lesquelles le profileur veut recevoir des notifications du CLR.</span><span class="sxs-lookup"><span data-stu-id="4a500-109">Gets the current event categories for which the profiler wants to receive notifications from the CLR.</span></span>|  
|[<span data-ttu-id="4a500-110">SetEventMask2, méthode</span><span class="sxs-lookup"><span data-stu-id="4a500-110">SetEventMask2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md)|<span data-ttu-id="4a500-111">Définit une valeur qui spécifie les types d'événements pour lesquels le profileur veut recevoir des notifications d'événements du CLR.</span><span class="sxs-lookup"><span data-stu-id="4a500-111">Sets a value that specifies the types of events for which the profiler wants to receive event notifications from the CLR.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4a500-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4a500-112">Remarks</span></span>  
 <span data-ttu-id="4a500-113">Les méthodes disponibles sur cette interface sont destinés à remplacer le [ICorProfilerInfo::GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) et [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) méthodes.</span><span class="sxs-lookup"><span data-stu-id="4a500-113">The methods available on this interface are intended to replace the [ICorProfilerInfo::GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) and [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a500-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4a500-114">Requirements</span></span>  
 <span data-ttu-id="4a500-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4a500-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a500-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="4a500-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="4a500-117">**Versions du .NET framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4a500-117">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a500-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a500-118">See Also</span></span>  
 [<span data-ttu-id="4a500-119">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="4a500-119">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
