---
title: ICorProfilerCallback3::InitializeForAttach, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback3.InitializeForAttach Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback3::InitializeForAttach
helpviewer_keywords:
- InitializeForAttach method [.NET Framework profiling]
- ICorProfilerCallback3::InitializeForAttach method [.NET Framework profiling]
ms.assetid: bed097b3-6d52-46c9-bee7-ac7910b6fc3f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 84d07fe975bab1b0af81299893b52142630b5bb9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59079745"
---
# <a name="icorprofilercallback3initializeforattach-method"></a><span data-ttu-id="6d56e-102">ICorProfilerCallback3::InitializeForAttach, méthode</span><span class="sxs-lookup"><span data-stu-id="6d56e-102">ICorProfilerCallback3::InitializeForAttach Method</span></span>
<span data-ttu-id="6d56e-103">Appelée par le Common Language Runtime (CLR) pour permettre au profileur d’initialiser son état après une opération d’attachement.</span><span class="sxs-lookup"><span data-stu-id="6d56e-103">Called by the common language runtime (CLR) to give the profiler an opportunity to initialize its state after an attach operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6d56e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d56e-104">Syntax</span></span>  
  
```  
HRESULT InitializeForAttach(  
            [in] IUnknown * pCorProfilerInfoUnk,  
            [in] void * pvClientData,  
            [in] UINT cbClientData);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6d56e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d56e-105">Parameters</span></span>  
 `pCorProfilerInfoUnk`  
 <span data-ttu-id="6d56e-106">[in] Pointeur d'interface pour l'interface `ICorProfilerInfo*`.</span><span class="sxs-lookup"><span data-stu-id="6d56e-106">[in] An interface pointer for the `ICorProfilerInfo*` interface.</span></span>  
  
 `pvClientData`  
 <span data-ttu-id="6d56e-107">[in] Un pointeur vers les données passées à la [IClrProfiling::AttachProfiler](../../../../docs/framework/unmanaged-api/profiling/iclrprofiling-attachprofiler-method.md) méthode dans son `pvClientData` paramètre.</span><span class="sxs-lookup"><span data-stu-id="6d56e-107">[in] A pointer to the data passed to the [IClrProfiling::AttachProfiler](../../../../docs/framework/unmanaged-api/profiling/iclrprofiling-attachprofiler-method.md) method in its `pvClientData` parameter.</span></span> <span data-ttu-id="6d56e-108">Si ce paramètre est null, `cbClientData` est égal à 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="6d56e-108">If this parameter is null, `cbClientData` will be 0 (zero).</span></span> <span data-ttu-id="6d56e-109">Le CLR libère cette mémoire au retour de `InitializeForAttach`.</span><span class="sxs-lookup"><span data-stu-id="6d56e-109">The CLR frees this memory when it returns from `InitializeForAttach`.</span></span>  
  
 `cbClientData`  
 <span data-ttu-id="6d56e-110">[in] Taille, en octets, des données vers lesquelles `pvClientData` pointe.</span><span class="sxs-lookup"><span data-stu-id="6d56e-110">[in] The size, in bytes, of the data that `pvClientData` points to.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6d56e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6d56e-111">Remarks</span></span>  
 <span data-ttu-id="6d56e-112">Le CLR appelle `InitializeForAttach` pour permettre au profileur de demander des rappels.</span><span class="sxs-lookup"><span data-stu-id="6d56e-112">The CLR calls `InitializeForAttach` to give the profiler an opportunity to request callbacks.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6d56e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d56e-113">Requirements</span></span>  
 <span data-ttu-id="6d56e-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6d56e-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6d56e-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="6d56e-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="6d56e-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6d56e-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="6d56e-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="6d56e-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="6d56e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d56e-118">See also</span></span>

- [<span data-ttu-id="6d56e-119">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="6d56e-119">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="6d56e-120">ICorProfilerInfo3, interface</span><span class="sxs-lookup"><span data-stu-id="6d56e-120">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [<span data-ttu-id="6d56e-121">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="6d56e-121">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="6d56e-122">Profilage</span><span class="sxs-lookup"><span data-stu-id="6d56e-122">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
