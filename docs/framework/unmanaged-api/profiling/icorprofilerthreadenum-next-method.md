---
title: ICorProfilerThreadEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum.Next
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum::Next
helpviewer_keywords:
- ICorProfilerThreadEnum::Next method [.NET Framework profiling]
- Next method, ICorProfilerThreadEnum interface [.NET Framework profiling]
ms.assetid: f3535279-3c63-41a2-ab0e-a129dc5a01e8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 44595229eaefa0d8fc8ca7bf15a88d0fbf1ee0d7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59104310"
---
# <a name="icorprofilerthreadenumnext-method"></a><span data-ttu-id="e4197-102">ICorProfilerThreadEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="e4197-102">ICorProfilerThreadEnum::Next Method</span></span>
<span data-ttu-id="e4197-103">Obtient le nombre spécifié de threads contigus dans une collection séquentielle de threads, à commencer par la position actuelle de l’énumérateur dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="e4197-103">Gets the specified number of contiguous threads from a sequential collection of threads, starting at the enumerator's current position in the sequence.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4197-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4197-104">Syntax</span></span>  
  
```  
HRESULT Next (    [in]  ULONG      celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
                    ThreadID ids[],  
    [out] ULONG *   pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e4197-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4197-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="e4197-106">[in] Nombre de threads à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e4197-106">[in] The number of threads to retrieve.</span></span>  
  
 `ids`  
 <span data-ttu-id="e4197-107">[out] Tableau de valeurs `ThreadID` qui représentent chacune un thread récupéré.</span><span class="sxs-lookup"><span data-stu-id="e4197-107">[out] An array of `ThreadID` values, each of which represents a retrieved thread.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="e4197-108">[out] Pointeur vers le nombre de threads<bpt i="1000001" x="1000001" type="formatting">{b&gt;</bpt><ept i="1000001">&lt;b}</ept>réellement retournés dans le tableau `ids`.</span><span class="sxs-lookup"><span data-stu-id="e4197-108">[out] A pointer to the number of threads actually returned in the `ids` array.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e4197-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e4197-109">Return Value</span></span>  
 <span data-ttu-id="e4197-110">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="e4197-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="e4197-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e4197-111">HRESULT</span></span>|<span data-ttu-id="e4197-112">Description</span><span class="sxs-lookup"><span data-stu-id="e4197-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e4197-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e4197-113">S_OK</span></span>|<span data-ttu-id="e4197-114">`celt` éléments ont été retournés.</span><span class="sxs-lookup"><span data-stu-id="e4197-114">`celt` elements were returned.</span></span>|  
|<span data-ttu-id="e4197-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e4197-115">S_FALSE</span></span>|<span data-ttu-id="e4197-116">Moins de `celt` éléments ont été retournés, ce qui indique que l'énumération est terminée.</span><span class="sxs-lookup"><span data-stu-id="e4197-116">Fewer than `celt` elements were returned, which indicates that the enumeration is complete.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e4197-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4197-117">Requirements</span></span>  
 <span data-ttu-id="e4197-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e4197-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4197-119">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e4197-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e4197-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e4197-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e4197-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4197-121">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4197-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4197-122">See also</span></span>

- [<span data-ttu-id="e4197-123">ICorProfilerThreadEnum, interface</span><span class="sxs-lookup"><span data-stu-id="e4197-123">ICorProfilerThreadEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="e4197-124">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="e4197-124">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
