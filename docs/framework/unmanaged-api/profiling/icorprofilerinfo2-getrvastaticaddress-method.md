---
title: ICorProfilerInfo2::GetRVAStaticAddress, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetRVAStaticAddress
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetRVAStaticAddress
helpviewer_keywords:
- GetRVAStaticAddress method [.NET Framework profiling]
- ICorProfilerInfo2::GetRVAStaticAddress method [.NET Framework profiling]
ms.assetid: a25a8f8b-5cfa-440d-9376-a1a1c3a9fc11
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9390fd62e001b02b6b6d758bb65a45ab847e89c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564092"
---
# <a name="icorprofilerinfo2getrvastaticaddress-method"></a><span data-ttu-id="6e850-102">ICorProfilerInfo2::GetRVAStaticAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="6e850-102">ICorProfilerInfo2::GetRVAStaticAddress Method</span></span>
<span data-ttu-id="6e850-103">Obtient l’adresse du champ statique d’adresse virtuelle relative (RVA) spécifié.</span><span class="sxs-lookup"><span data-stu-id="6e850-103">Gets the address of the specified relative virtual address (RVA) static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e850-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e850-104">Syntax</span></span>  
  
```  
HRESULT GetRVAStaticAddress(  
    [in] ClassID classId,  
    [in] mdFieldDef fieldToken,  
    [out] void **ppAddress);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6e850-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e850-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="6e850-106">[in] ID de la classe qui contient le champ statique RVA demandé.</span><span class="sxs-lookup"><span data-stu-id="6e850-106">[in] The ID of the class that contains the requested RVA-static field.</span></span>  
  
 `fieldToken`  
 <span data-ttu-id="6e850-107">[in] Jeton de métadonnées pour le champ statique RVA demandé.</span><span class="sxs-lookup"><span data-stu-id="6e850-107">[in] Metadata token for the requested RVA-static field.</span></span>  
  
 `ppAddress`  
 <span data-ttu-id="6e850-108">[out] Pointeur vers l’adresse du champ statique RVA.</span><span class="sxs-lookup"><span data-stu-id="6e850-108">[out] A pointer to the address of the RVA-static field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6e850-109">Notes</span><span class="sxs-lookup"><span data-stu-id="6e850-109">Remarks</span></span>  
 <span data-ttu-id="6e850-110">Le `GetRVAStaticAddress` méthode peut retourner l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e850-110">The `GetRVAStaticAddress` method may return one of the following:</span></span>  
  
-   <span data-ttu-id="6e850-111">Un HRESULT CORPROF_E_DATAINCOMPLETE si le champ statique donné n’a pas été assigné une adresse dans le contexte spécifié.</span><span class="sxs-lookup"><span data-stu-id="6e850-111">A CORPROF_E_DATAINCOMPLETE HRESULT if the given static field has not been assigned an address in the specified context.</span></span>  
  
-   <span data-ttu-id="6e850-112">Les adresses des objets qui peuvent être dans le tas de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="6e850-112">The addresses of objects that may be in the garbage collection heap.</span></span> <span data-ttu-id="6e850-113">Ces adresses peuvent devenir non valides après le garbage collection, donc après le garbage collection, les profileurs ne doivent pas supposer qu’ils sont valides.</span><span class="sxs-lookup"><span data-stu-id="6e850-113">These addresses may become invalid after garbage collection, so after garbage collection, profilers should not assume that they are valid.</span></span>  
  
 <span data-ttu-id="6e850-114">Avant la fin de constructeur de classe d’une classe, `GetRVAStaticAddress` retournera CORPROF_E_DATAINCOMPLETE pour tous ses champs statiques, bien que certains des champs statiques peuvent déjà être initialisés et utiliser des objets de garbage collection à la racine.</span><span class="sxs-lookup"><span data-stu-id="6e850-114">Before a class’s class constructor is completed, `GetRVAStaticAddress` will return CORPROF_E_DATAINCOMPLETE for all its static fields, although some of the static fields may already be initialized and may be rooting garbage collection objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6e850-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6e850-115">Requirements</span></span>  
 <span data-ttu-id="6e850-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6e850-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6e850-117">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="6e850-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="6e850-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6e850-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6e850-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6e850-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e850-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e850-120">See also</span></span>
- [<span data-ttu-id="6e850-121">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="6e850-121">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="6e850-122">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="6e850-122">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
