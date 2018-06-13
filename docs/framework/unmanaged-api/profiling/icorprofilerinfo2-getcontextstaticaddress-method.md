---
title: ICorProfilerInfo2::GetContextStaticAddress, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetContextStaticAddress
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetContextStaticAddress
helpviewer_keywords:
- GetContextStaticAddress method [.NET Framework profiling]
- ICorProfilerInfo2::GetContextStaticAddress method [.NET Framework profiling]
ms.assetid: 2b374116-0972-416a-8cf5-79213129be9a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d787e3eae59218c46a95c327a0f93502c3833d9b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33456233"
---
# <a name="icorprofilerinfo2getcontextstaticaddress-method"></a><span data-ttu-id="2a8f8-102">ICorProfilerInfo2::GetContextStaticAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="2a8f8-102">ICorProfilerInfo2::GetContextStaticAddress Method</span></span>
<span data-ttu-id="2a8f8-103">Obtient l’adresse pour le champ statique de contexte spécifié qui est dans la portée du contexte spécifié.</span><span class="sxs-lookup"><span data-stu-id="2a8f8-103">Gets the address for the specified context-static field that is in the scope of the specified context.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a8f8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a8f8-104">Syntax</span></span>  
  
```  
HRESULT GetContextStaticAddress(  
    [in] ClassID classId,  
    [in] mdFieldDef fieldToken,  
    [in] ContextID contextId,  
    [out] void **ppAddress);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2a8f8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a8f8-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="2a8f8-106">[in] L’ID de la classe qui contient le champ statique de contexte demandé.</span><span class="sxs-lookup"><span data-stu-id="2a8f8-106">[in] The ID of the class that contains the requested context-static field.</span></span>  
  
 `fieldToken`  
 <span data-ttu-id="2a8f8-107">[in] Le jeton de métadonnées pour le champ statique de contexte demandé.</span><span class="sxs-lookup"><span data-stu-id="2a8f8-107">[in] The metadata token for the requested context-static field.</span></span>  
  
 `contextId`  
 <span data-ttu-id="2a8f8-108">[in] L’ID du contexte qui est la portée pour le champ statique de contexte demandé.</span><span class="sxs-lookup"><span data-stu-id="2a8f8-108">[in] The ID of the context that is the scope for the requested context-static field.</span></span>  
  
 `ppAddress`  
 <span data-ttu-id="2a8f8-109">[out] Pointeur vers l’adresse du champ statique qui est dans le contexte spécifié.</span><span class="sxs-lookup"><span data-stu-id="2a8f8-109">[out] A pointer to the address of the static field that is within the specified context.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2a8f8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2a8f8-110">Remarks</span></span>  
 <span data-ttu-id="2a8f8-111">Le `GetContextStaticAddress` méthode peut retourner l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a8f8-111">The `GetContextStaticAddress` method may return one of the following:</span></span>  
  
-   <span data-ttu-id="2a8f8-112">Un CORPROF_E_DATAINCOMPLETE HRESULT si le champ statique donné n’a pas été affecté une adresse dans le contexte spécifié.</span><span class="sxs-lookup"><span data-stu-id="2a8f8-112">A CORPROF_E_DATAINCOMPLETE HRESULT if the given static field has not been assigned an address in the specified context.</span></span>  
  
-   <span data-ttu-id="2a8f8-113">Les adresses des objets qui peuvent être dans le tas de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="2a8f8-113">The addresses of objects that may be in the garbage collection heap.</span></span> <span data-ttu-id="2a8f8-114">Ces adresses peuvent devenir non valides après le garbage collection, donc après le garbage collection, les profileurs ne doivent pas supposer qu’ils sont valides.</span><span class="sxs-lookup"><span data-stu-id="2a8f8-114">These addresses may become invalid after garbage collection, so after garbage collection, profilers should not assume that they are valid.</span></span>  
  
 <span data-ttu-id="2a8f8-115">Avant la fin de constructeur de classe d’une classe, `GetContextStaticAddress` retournera CORPROF_E_DATAINCOMPLETE pour tous ses champs statiques, bien que certains champs statiques peuvent déjà être initialisés et utiliser des objets de garbage collection racine.</span><span class="sxs-lookup"><span data-stu-id="2a8f8-115">Before a class’s class constructor is completed, `GetContextStaticAddress` will return CORPROF_E_DATAINCOMPLETE for all its static fields, although some of the static fields may already be initialized and rooting garbage collection objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2a8f8-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2a8f8-116">Requirements</span></span>  
 <span data-ttu-id="2a8f8-117">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2a8f8-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2a8f8-118">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2a8f8-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2a8f8-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2a8f8-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2a8f8-120">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2a8f8-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a8f8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a8f8-121">See Also</span></span>  
 [<span data-ttu-id="2a8f8-122">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="2a8f8-122">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="2a8f8-123">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="2a8f8-123">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
