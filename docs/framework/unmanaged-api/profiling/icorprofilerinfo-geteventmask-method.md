---
title: ICorProfilerInfo::GetEventMask, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetEventMask
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetEventMask
helpviewer_keywords:
- GetEventMask method [.NET Framework profiling]
- ICorProfilerInfo::GetEventMask method [.NET Framework profiling]
ms.assetid: ec34cc13-45a3-4695-abc3-b3347d4e6fc2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e2881dbe83b0d9f6e2ae3c4f478bbecdca444b78
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59076531"
---
# <a name="icorprofilerinfogeteventmask-method"></a><span data-ttu-id="3f4a8-102">ICorProfilerInfo::GetEventMask, méthode</span><span class="sxs-lookup"><span data-stu-id="3f4a8-102">ICorProfilerInfo::GetEventMask Method</span></span>
<span data-ttu-id="3f4a8-103">Obtient les catégories des événements actifs pour lesquelles le profileur veut recevoir des notifications d'événement du CLR.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-103">Gets the current event categories for which the profiler wants to receive event notifications from the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f4a8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f4a8-104">Syntax</span></span>  
  
```  
HRESULT GetEventMask(  
    [out] DWORD *pdwEvents);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3f4a8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f4a8-105">Parameters</span></span>  
 `pdwEvents`  
 <span data-ttu-id="3f4a8-106">[en sortie] Un pointeur vers une valeur de 4 octets qui spécifie les catégories des événements.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-106">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="3f4a8-107">Chaque bit contrôle une fonctionnalité, un comportement ou un type d'événement différents.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-107">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="3f4a8-108">Les bits sont décrits dans le [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-108">The bits are described in the [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3f4a8-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3f4a8-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3f4a8-110">Vous devez appeler la [GetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-geteventmask2-method.md) méthode au lieu de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-110">You should call the [GetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-geteventmask2-method.md) method instead of this method.</span></span> <span data-ttu-id="3f4a8-111">Bien que le `SetEventMask` méthode continue à être pris en charge, [GetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-geteventmask2-method.md) fournit des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-111">Although the `SetEventMask` method continues to be supported, [GetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-geteventmask2-method.md) provides additional functionality.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f4a8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f4a8-112">Requirements</span></span>  
 <span data-ttu-id="3f4a8-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3f4a8-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3f4a8-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3f4a8-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3f4a8-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3f4a8-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="3f4a8-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="3f4a8-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3f4a8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f4a8-117">See also</span></span>

- [<span data-ttu-id="3f4a8-118">GetEventMask2, méthode</span><span class="sxs-lookup"><span data-stu-id="3f4a8-118">GetEventMask2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-geteventmask2-method.md)
- [<span data-ttu-id="3f4a8-119">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="3f4a8-119">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
