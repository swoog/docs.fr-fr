---
title: ICorProfilerInfo5::SetEventMask2, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- IcorProfilerInfo5.SetEventMask2
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: 05dbbe2b-049c-4a60-be69-2ad7a949405e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 266219894ffefa0d4066c6ca68c7cadf6265e098
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59175810"
---
# <a name="icorprofilerinfo5seteventmask2-method"></a><span data-ttu-id="c13e7-102">ICorProfilerInfo5::SetEventMask2, méthode</span><span class="sxs-lookup"><span data-stu-id="c13e7-102">ICorProfilerInfo5::SetEventMask2 Method</span></span>
<span data-ttu-id="c13e7-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="c13e7-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="c13e7-104">Définit une valeur qui spécifie les types d'événements pour lesquels le profileur veut recevoir des notifications d'événements du CLR (Common Language Runtime).</span><span class="sxs-lookup"><span data-stu-id="c13e7-104">Sets a value that specifies the types of events for which the profiler wants to receive event notifications from the common language runtime (CLR).</span></span> <span data-ttu-id="c13e7-105">Il fournit davantage de fonctionnalités que le [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="c13e7-105">It provides more functionality than the [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c13e7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c13e7-106">Syntax</span></span>  
  
```cpp
HRESULT SetEventMask2(        [in] DWORD dwEventsLow,        [in] DWORD dwEventsHigh  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c13e7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c13e7-107">Parameters</span></span>  
 `dwEventsLow`  
 <span data-ttu-id="c13e7-108">[en entrée] Une valeur de 4 octets qui spécifie les catégories des événements.</span><span class="sxs-lookup"><span data-stu-id="c13e7-108">[in] A 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="c13e7-109">Chaque bit contrôle une fonctionnalité, un comportement ou un type d'événement différents.</span><span class="sxs-lookup"><span data-stu-id="c13e7-109">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="c13e7-110">Les bits sont décrits dans le [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="c13e7-110">The bits are described in the [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
 `dwEventsHigh`  
 <span data-ttu-id="c13e7-111">[en entrée] Une valeur de 4 octets qui spécifie les catégories des événements.</span><span class="sxs-lookup"><span data-stu-id="c13e7-111">[in] A 4-byte value that specifies the categories of events.</span></span>  <span data-ttu-id="c13e7-112">Chaque bit contrôle une fonctionnalité, un comportement ou un type d'événement différents.</span><span class="sxs-lookup"><span data-stu-id="c13e7-112">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="c13e7-113">Les bits sont décrits dans le [COR_PRF_HIGH_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="c13e7-113">The bits are described in the [COR_PRF_HIGH_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c13e7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c13e7-114">Remarks</span></span>  
 <span data-ttu-id="c13e7-115">La méthode `SetEventMask2` est utilisée pour définir les rappels auxquels le profileur s'abonne.</span><span class="sxs-lookup"><span data-stu-id="c13e7-115">The `SetEventMask2` method is used to set the callbacks to which the profiler subscribes.</span></span> <span data-ttu-id="c13e7-116">En règle générale, vous appelez le [GetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-geteventmask2-method.md) méthode pour déterminer les bits sont définis, effectuer une opération OR logique de ses `pdwEventsLow` et `pdwEventsHigh` valeurs et des nouveaux bits que vous souhaitez définir, puis appelez le `SetEventMask2` (méthode).</span><span class="sxs-lookup"><span data-stu-id="c13e7-116">Typically, you call the [GetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-geteventmask2-method.md) method to determine which bits are set, perform a logical OR of its `pdwEventsLow` and `pdwEventsHigh` values and any new bits you want to set, and then call the `SetEventMask2` method.</span></span>  
  
 <span data-ttu-id="c13e7-117">Cette méthode est l’alternative recommandée à la [SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="c13e7-117">This method is the recommended alternative to the [SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c13e7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c13e7-118">Requirements</span></span>  
 <span data-ttu-id="c13e7-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c13e7-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c13e7-120">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c13e7-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c13e7-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c13e7-121">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="c13e7-122">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c13e7-122">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c13e7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c13e7-123">See also</span></span>

- [<span data-ttu-id="c13e7-124">ICorProfilerInfo5, interface</span><span class="sxs-lookup"><span data-stu-id="c13e7-124">ICorProfilerInfo5 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-interface.md)
- [<span data-ttu-id="c13e7-125">GetEventMask2, méthode</span><span class="sxs-lookup"><span data-stu-id="c13e7-125">GetEventMask2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-geteventmask2-method.md)
