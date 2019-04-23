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
ms.openlocfilehash: f8ebddf9a16b2eddbbc58342f68b517064e8d794
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59214635"
---
# <a name="icorprofilerinfo5geteventmask2-method"></a><span data-ttu-id="442bf-102">ICorProfilerInfo5::GetEventMask2, méthode</span><span class="sxs-lookup"><span data-stu-id="442bf-102">ICorProfilerInfo5::GetEventMask2 Method</span></span>
<span data-ttu-id="442bf-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="442bf-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="442bf-104">Obtient les catégories des événements actifs pour lesquelles le profileur veut recevoir des notifications du CLR.</span><span class="sxs-lookup"><span data-stu-id="442bf-104">Gets the current event categories for which the profiler wants to receive notifications from the common language runtime (CLR).</span></span>  <span data-ttu-id="442bf-105">Il fournit des fonctionnalités non fournies par le [ICorProfilerInfo::GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="442bf-105">It provides functionality not provided by the [ICorProfilerInfo::GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="442bf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="442bf-106">Syntax</span></span>  
  
```cpp
HRESULT GetEventMask2(  
        [out] DWORD* pdwEventsLow,  
        [out] DWORD* pdwEventsHigh  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="442bf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="442bf-107">Parameters</span></span>  
 `pdwEventsLow`  
 <span data-ttu-id="442bf-108">[en sortie] Un pointeur vers une valeur de 4 octets qui spécifie les catégories des événements.</span><span class="sxs-lookup"><span data-stu-id="442bf-108">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="442bf-109">Chaque bit contrôle une fonctionnalité, un comportement ou un type d'événement différents.</span><span class="sxs-lookup"><span data-stu-id="442bf-109">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="442bf-110">Les bits sont décrits dans le [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="442bf-110">The bits are described in the [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
 `pdwEventsHigh`  
 <span data-ttu-id="442bf-111">[en sortie] Un pointeur vers une valeur de 4 octets qui spécifie les catégories des événements.</span><span class="sxs-lookup"><span data-stu-id="442bf-111">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span>  <span data-ttu-id="442bf-112">Chaque bit contrôle une fonctionnalité, un comportement ou un type d'événement différents.</span><span class="sxs-lookup"><span data-stu-id="442bf-112">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="442bf-113">Les bits sont décrits dans le [COR_PRF_HIGH_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="442bf-113">The bits are described in the [COR_PRF_HIGH_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="442bf-114">Notes</span><span class="sxs-lookup"><span data-stu-id="442bf-114">Remarks</span></span>  
 <span data-ttu-id="442bf-115">La méthode `GetEventMask2` est utilisée pour déterminer les rappels auxquels le profileur s'est abonné.</span><span class="sxs-lookup"><span data-stu-id="442bf-115">The `GetEventMask2` method is used to determine which callbacks the profiler has subscribed to.</span></span> <span data-ttu-id="442bf-116">En général, vous effectuez une opération OR logique de la `pdwEventsLow` et `pdwEventsHigh` valeurs et des nouveaux bits que vous souhaitez définir, puis appelez le [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="442bf-116">Typically, you perform a logical OR of the `pdwEventsLow` and `pdwEventsHigh` values and any new bits you want to set, and then call the [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) method.</span></span>  
  
 <span data-ttu-id="442bf-117">Cette méthode est l’alternative recommandée à la [GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="442bf-117">This method is the recommended alternative to the [GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="442bf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="442bf-118">Requirements</span></span>  
 <span data-ttu-id="442bf-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="442bf-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="442bf-120">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="442bf-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="442bf-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="442bf-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="442bf-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="442bf-122">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="442bf-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="442bf-123">See also</span></span>

- [<span data-ttu-id="442bf-124">ICorProfilerInfo5, interface</span><span class="sxs-lookup"><span data-stu-id="442bf-124">ICorProfilerInfo5 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-interface.md)
- [<span data-ttu-id="442bf-125">SetEventMask2, méthode</span><span class="sxs-lookup"><span data-stu-id="442bf-125">SetEventMask2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md)
