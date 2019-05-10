---
title: ICorProfilerInfo2::GetThreadStaticAddress, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetThreadStaticAddress
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetThreadStaticAddress
helpviewer_keywords:
- GetThreadStaticAddress method [.NET Framework profiling]
- ICorProfilerInfo2::GetThreadStaticAddress method [.NET Framework profiling]
ms.assetid: 8e7dbf14-98a2-4384-a950-58a7640e59df
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: de0e46f4703479daeb96cb83276ec14150125e7f
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64587441"
---
# <a name="icorprofilerinfo2getthreadstaticaddress-method"></a><span data-ttu-id="5f1d7-102">ICorProfilerInfo2::GetThreadStaticAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="5f1d7-102">ICorProfilerInfo2::GetThreadStaticAddress Method</span></span>
<span data-ttu-id="5f1d7-103">Obtient l’adresse du champ statique de thread spécifié qui est dans la portée du thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="5f1d7-103">Gets the address of the specified thread-static field that is in the scope of the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f1d7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f1d7-104">Syntax</span></span>  
  
```  
HRESULT GetThreadStaticAddress(  
    [in] ClassID     classId,  
    [in] mdFieldDef  fieldToken,  
    [in] ThreadID    threadId,  
    [out] void       **ppAddress);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5f1d7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f1d7-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="5f1d7-106">[in] ID de la classe qui contient le champ thread-static demandé.</span><span class="sxs-lookup"><span data-stu-id="5f1d7-106">[in] The ID of the class that contains the requested thread-static field.</span></span>  
  
 `fieldToken`  
 <span data-ttu-id="5f1d7-107">[in] Le jeton de métadonnées pour le champ statique de thread demandé.</span><span class="sxs-lookup"><span data-stu-id="5f1d7-107">[in] The metadata token for the requested thread-static field.</span></span>  
  
 `threadId`  
 <span data-ttu-id="5f1d7-108">[in] L’ID du thread qui est la portée pour le champ statique demandé.</span><span class="sxs-lookup"><span data-stu-id="5f1d7-108">[in] The ID of the thread that is the scope for the requested static field.</span></span>  
  
 `ppAddress`  
 <span data-ttu-id="5f1d7-109">[out] Pointeur vers l’adresse du champ statique qui se trouve dans le thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="5f1d7-109">[out] A pointer to the address of the static field that is within the specified thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5f1d7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5f1d7-110">Remarks</span></span>  
 <span data-ttu-id="5f1d7-111">Le `GetThreadStaticAddress` méthode peut retourner l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f1d7-111">The `GetThreadStaticAddress` method may return one of the following:</span></span>  
  
- <span data-ttu-id="5f1d7-112">Un HRESULT CORPROF_E_DATAINCOMPLETE si le champ statique donné n’a pas été assigné une adresse dans le contexte spécifié.</span><span class="sxs-lookup"><span data-stu-id="5f1d7-112">A CORPROF_E_DATAINCOMPLETE HRESULT if the given static field has not been assigned an address in the specified context.</span></span>  
  
- <span data-ttu-id="5f1d7-113">Les adresses des objets qui peuvent être dans le tas de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="5f1d7-113">The addresses of objects that may be in the garbage collection heap.</span></span> <span data-ttu-id="5f1d7-114">Ces adresses peuvent devenir non valides après le garbage collection, après que les profileurs de garbage collection ne doivent pas supposer qu’ils sont valides.</span><span class="sxs-lookup"><span data-stu-id="5f1d7-114">These addresses may become invalid after garbage collection, so after garbage collection profilers should not assume that they are valid.</span></span>  
  
 <span data-ttu-id="5f1d7-115">Avant la fin de constructeur de classe d’une classe, `GetThreadStaticAddress` retournera CORPROF_E_DATAINCOMPLETE pour tous ses champs statiques, bien que certains des champs statiques peuvent déjà être initialisés et utiliser des objets de garbage collection racine.</span><span class="sxs-lookup"><span data-stu-id="5f1d7-115">Before a class’s class constructor is completed, `GetThreadStaticAddress` will return CORPROF_E_DATAINCOMPLETE for all its static fields, although some of the static fields may already be initialized and rooting garbage collection objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f1d7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f1d7-116">Requirements</span></span>  
 <span data-ttu-id="5f1d7-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5f1d7-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f1d7-118">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5f1d7-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5f1d7-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5f1d7-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5f1d7-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f1d7-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f1d7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f1d7-121">See also</span></span>

- [<span data-ttu-id="5f1d7-122">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="5f1d7-122">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="5f1d7-123">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="5f1d7-123">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
