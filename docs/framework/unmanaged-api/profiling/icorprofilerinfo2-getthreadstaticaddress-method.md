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
ms.openlocfilehash: 3574d7e889481931f40dbfb3158ad523c7e5637e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54534993"
---
# <a name="icorprofilerinfo2getthreadstaticaddress-method"></a><span data-ttu-id="dbfb0-102">ICorProfilerInfo2::GetThreadStaticAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="dbfb0-102">ICorProfilerInfo2::GetThreadStaticAddress Method</span></span>
<span data-ttu-id="dbfb0-103">Obtient l’adresse du champ statique de thread spécifié qui est dans la portée du thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-103">Gets the address of the specified thread-static field that is in the scope of the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dbfb0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbfb0-104">Syntax</span></span>  
  
```  
HRESULT GetThreadStaticAddress(  
    [in] ClassID     classId,  
    [in] mdFieldDef  fieldToken,  
    [in] ThreadID    threadId,  
    [out] void       **ppAddress);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dbfb0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbfb0-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="dbfb0-106">[in] ID de la classe qui contient le champ thread-static demandé.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-106">[in] The ID of the class that contains the requested thread-static field.</span></span>  
  
 `fieldToken`  
 <span data-ttu-id="dbfb0-107">[in] Le jeton de métadonnées pour le champ statique de thread demandé.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-107">[in] The metadata token for the requested thread-static field.</span></span>  
  
 `threadId`  
 <span data-ttu-id="dbfb0-108">[in] L’ID du thread qui est la portée pour le champ statique demandé.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-108">[in] The ID of the thread that is the scope for the requested static field.</span></span>  
  
 `ppAddress`  
 <span data-ttu-id="dbfb0-109">[out] Pointeur vers l’adresse du champ statique qui se trouve dans le thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-109">[out] A pointer to the address of the static field that is within the specified thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dbfb0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="dbfb0-110">Remarks</span></span>  
 <span data-ttu-id="dbfb0-111">Le `GetThreadStaticAddress` méthode peut retourner l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbfb0-111">The `GetThreadStaticAddress` method may return one of the following:</span></span>  
  
-   <span data-ttu-id="dbfb0-112">Un HRESULT CORPROF_E_DATAINCOMPLETE si le champ statique donné n’a pas été assigné une adresse dans le contexte spécifié.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-112">A CORPROF_E_DATAINCOMPLETE HRESULT if the given static field has not been assigned an address in the specified context.</span></span>  
  
-   <span data-ttu-id="dbfb0-113">Les adresses des objets qui peuvent être dans le tas de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-113">The addresses of objects that may be in the garbage collection heap.</span></span> <span data-ttu-id="dbfb0-114">Ces adresses peuvent devenir non valides après le garbage collection, après que les profileurs de garbage collection ne doivent pas supposer qu’ils sont valides.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-114">These addresses may become invalid after garbage collection, so after garbage collection profilers should not assume that they are valid.</span></span>  
  
 <span data-ttu-id="dbfb0-115">Avant la fin de constructeur de classe d’une classe, `GetThreadStaticAddress` retournera CORPROF_E_DATAINCOMPLETE pour tous ses champs statiques, bien que certains des champs statiques peuvent déjà être initialisés et utiliser des objets de garbage collection racine.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-115">Before a class’s class constructor is completed, `GetThreadStaticAddress` will return CORPROF_E_DATAINCOMPLETE for all its static fields, although some of the static fields may already be initialized and rooting garbage collection objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dbfb0-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dbfb0-116">Requirements</span></span>  
 <span data-ttu-id="dbfb0-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dbfb0-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dbfb0-118">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="dbfb0-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="dbfb0-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dbfb0-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dbfb0-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dbfb0-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dbfb0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbfb0-121">See also</span></span>
- [<span data-ttu-id="dbfb0-122">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="dbfb0-122">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="dbfb0-123">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="dbfb0-123">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
