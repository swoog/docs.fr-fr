---
title: ICorProfilerInfo5::GetEventMask2, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorProfilerInfo5.GetEventMask2
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: f854b68f-009c-4ffb-89cd-ca874d1c0fb7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8973e100694be0f50b575d978f3327b8b3a1d334
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455662"
---
# <a name="icorprofilerinfo5geteventmask2-method"></a><span data-ttu-id="e95d1-102">ICorProfilerInfo5::GetEventMask2, méthode</span><span class="sxs-lookup"><span data-stu-id="e95d1-102">ICorProfilerInfo5::GetEventMask2 Method</span></span>
<span data-ttu-id="e95d1-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="e95d1-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="e95d1-104">Obtient les catégories des événements actifs pour lesquelles le profileur veut recevoir des notifications du CLR.</span><span class="sxs-lookup"><span data-stu-id="e95d1-104">Gets the current event categories for which the profiler wants to receive notifications from the common language runtime (CLR).</span></span>  <span data-ttu-id="e95d1-105">Il fournit des fonctionnalités non fournies par le [ICorProfilerInfo::GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="e95d1-105">It provides functionality not provided by the [ICorProfilerInfo::GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e95d1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e95d1-106">Syntax</span></span>  
  
```cpp
HRESULT GetEventMask2(  
        [out] DWORD* pdwEventsLow,  
        [out] DWORD* pdwEventsHigh  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e95d1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e95d1-107">Parameters</span></span>  
 `pdwEventsLow`  
 <span data-ttu-id="e95d1-108">[en sortie] Un pointeur vers une valeur de 4 octets qui spécifie les catégories des événements.</span><span class="sxs-lookup"><span data-stu-id="e95d1-108">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="e95d1-109">Chaque bit contrôle une fonctionnalité, un comportement ou un type d'événement différents.</span><span class="sxs-lookup"><span data-stu-id="e95d1-109">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="e95d1-110">Les bits sont décrits dans le [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="e95d1-110">The bits are described in the [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
 `pdwEventsHigh`  
 <span data-ttu-id="e95d1-111">[en sortie] Un pointeur vers une valeur de 4 octets qui spécifie les catégories des événements.</span><span class="sxs-lookup"><span data-stu-id="e95d1-111">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span>  <span data-ttu-id="e95d1-112">Chaque bit contrôle une fonctionnalité, un comportement ou un type d'événement différents.</span><span class="sxs-lookup"><span data-stu-id="e95d1-112">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="e95d1-113">Les bits sont décrits dans le [COR_PRF_HIGH_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="e95d1-113">The bits are described in the [COR_PRF_HIGH_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e95d1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e95d1-114">Remarks</span></span>  
 <span data-ttu-id="e95d1-115">La méthode `GetEventMask2` est utilisée pour déterminer les rappels auxquels le profileur s'est abonné.</span><span class="sxs-lookup"><span data-stu-id="e95d1-115">The `GetEventMask2` method is used to determine which callbacks the profiler has subscribed to.</span></span> <span data-ttu-id="e95d1-116">En règle générale, vous effectuez un ou logique de la `pdwEventsLow` et `pdwEventsHigh` valeurs et des nouveaux bits que vous souhaitez définir, puis appelez le [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="e95d1-116">Typically, you perform a logical OR of the `pdwEventsLow` and `pdwEventsHigh` values and any new bits you want to set, and then call the [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) method.</span></span>  
  
 <span data-ttu-id="e95d1-117">Cette méthode est l’alternative recommandée à la [GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="e95d1-117">This method is the recommended alternative to the [GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e95d1-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e95d1-118">Requirements</span></span>  
 <span data-ttu-id="e95d1-119">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e95d1-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e95d1-120">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e95d1-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e95d1-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e95d1-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e95d1-122">**Versions du .NET framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e95d1-122">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e95d1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e95d1-123">See Also</span></span>  
 [<span data-ttu-id="e95d1-124">ICorProfilerInfo5, interface</span><span class="sxs-lookup"><span data-stu-id="e95d1-124">ICorProfilerInfo5 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-interface.md)  
 [<span data-ttu-id="e95d1-125">SetEventMask2, méthode</span><span class="sxs-lookup"><span data-stu-id="e95d1-125">SetEventMask2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md)
