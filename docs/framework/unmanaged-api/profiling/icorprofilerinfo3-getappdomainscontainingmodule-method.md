---
title: ICorProfilerInfo3::GetAppDomainsContainingModule, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.GetAppDomainsContainingModule Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::GetAppDomainsContainingModule
helpviewer_keywords:
- GetAppDomainsContainingModule method [.NET Framework profiling]
- ICorProfilerInfo3::GetAppDomainsContainingModule method [.NET Framework profiling]
ms.assetid: 603b3881-ea94-4dca-95cd-91eebac873a0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b5658ac87c7a938381639442216df03853f02998
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59195785"
---
# <a name="icorprofilerinfo3getappdomainscontainingmodule-method"></a><span data-ttu-id="23ef7-102">ICorProfilerInfo3::GetAppDomainsContainingModule, méthode</span><span class="sxs-lookup"><span data-stu-id="23ef7-102">ICorProfilerInfo3::GetAppDomainsContainingModule Method</span></span>
<span data-ttu-id="23ef7-103">Obtient les identificateurs des domaines d'application dans lesquels le module donné a été chargé.</span><span class="sxs-lookup"><span data-stu-id="23ef7-103">Gets the identifiers of the application domains in which the given module has been loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="23ef7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23ef7-104">Syntax</span></span>  
  
```  
HRESULT GetAppDomainsContainingModule(  
            [in] ModuleID moduleId,  
            [in] ULONG32 cAppDomainIds,  
            [out] ULONG32 *pcAppDomainIds,  
            [out, size_is(cAppDomainIds), length_is(*pcAppDomainIds)]  
                    AppDomainID appDomainIds[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="23ef7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23ef7-105">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="23ef7-106">[in] ID du module chargé.</span><span class="sxs-lookup"><span data-stu-id="23ef7-106">[in] The ID of the loaded module.</span></span>  
  
 `cAppDomainIds`  
 <span data-ttu-id="23ef7-107">[in] Taille du tableau `appDomainIds`.</span><span class="sxs-lookup"><span data-stu-id="23ef7-107">[in] The size of the `appDomainIds` array.</span></span>  
  
 `pcAppDomainIds`  
 <span data-ttu-id="23ef7-108">[out] Pointeur vers le nombre total d'éléments retournés.</span><span class="sxs-lookup"><span data-stu-id="23ef7-108">[out] A pointer to the total number of returned elements.</span></span>  
  
 `appDomainIds`  
 <span data-ttu-id="23ef7-109">[out] Tableau de valeurs d'ID de domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="23ef7-109">[out] An array of application domain ID values.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="23ef7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="23ef7-110">Remarks</span></span>  
 <span data-ttu-id="23ef7-111">Cette méthode utilise des mémoires tampons allouées par l'appelant.</span><span class="sxs-lookup"><span data-stu-id="23ef7-111">The method uses caller allocated buffers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="23ef7-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23ef7-112">Requirements</span></span>  
 <span data-ttu-id="23ef7-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="23ef7-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="23ef7-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="23ef7-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="23ef7-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="23ef7-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="23ef7-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="23ef7-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="23ef7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23ef7-117">See also</span></span>

- [<span data-ttu-id="23ef7-118">ICorProfilerFunctionEnum, interface</span><span class="sxs-lookup"><span data-stu-id="23ef7-118">ICorProfilerFunctionEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md)
- [<span data-ttu-id="23ef7-119">ICorProfilerInfo3, interface</span><span class="sxs-lookup"><span data-stu-id="23ef7-119">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [<span data-ttu-id="23ef7-120">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="23ef7-120">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="23ef7-121">Profilage</span><span class="sxs-lookup"><span data-stu-id="23ef7-121">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
