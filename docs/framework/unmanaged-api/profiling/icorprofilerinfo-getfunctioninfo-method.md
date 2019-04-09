---
title: ICorProfilerInfo::GetFunctionInfo, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetFunctionInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetFunctionInfo
helpviewer_keywords:
- ICorProfilerInfo::GetFunctionInfo method [.NET Framework profiling]
- GetFunctionInfo method [.NET Framework profiling]
ms.assetid: c42b5891-019d-46b3-b551-4606295b75b8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4dd262c8206fdd45ca8a14f860a0894b999b0730
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59113605"
---
# <a name="icorprofilerinfogetfunctioninfo-method"></a><span data-ttu-id="2901d-102">ICorProfilerInfo::GetFunctionInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="2901d-102">ICorProfilerInfo::GetFunctionInfo Method</span></span>
<span data-ttu-id="2901d-103">Obtient la classe parente et les métadonnées de jeton pour la fonction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2901d-103">Gets the parent class and metadata token for the specified function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2901d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2901d-104">Syntax</span></span>  
  
```  
HRESULT GetFunctionInfo(  
    [in]  FunctionID functionId,  
    [out] ClassID    *pClassId,  
    [out] ModuleID   *pModuleId,  
    [out] mdToken    *pToken);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2901d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2901d-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="2901d-106">[in] L’ID de la fonction pour laquelle obtenir la classe parente et les métadonnées de jeton.</span><span class="sxs-lookup"><span data-stu-id="2901d-106">[in] The ID of the function for which to get the parent class and metadata token.</span></span>  
  
 `pClassId`  
 <span data-ttu-id="2901d-107">[out] Pointeur vers la classe parente de la fonction.</span><span class="sxs-lookup"><span data-stu-id="2901d-107">[out] A pointer to the parent class of the function.</span></span>  
  
 `pModuleId`  
 <span data-ttu-id="2901d-108">[out] Pointeur vers le module dans lequel la classe parente de la fonction est définie.</span><span class="sxs-lookup"><span data-stu-id="2901d-108">[out] A pointer to the module in which the function's parent class is defined.</span></span>  
  
 `pToken`  
 <span data-ttu-id="2901d-109">[out] Pointeur vers le jeton de métadonnées de la fonction.</span><span class="sxs-lookup"><span data-stu-id="2901d-109">[out] A pointer to the metadata token for the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2901d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2901d-110">Remarks</span></span>  
 <span data-ttu-id="2901d-111">Le code de profileur peut appeler [ICorProfilerInfo::GetModuleMetaData](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getmodulemetadata-method.md) pour obtenir une interface de métadonnées pour un module donné.</span><span class="sxs-lookup"><span data-stu-id="2901d-111">The profiler code can call [ICorProfilerInfo::GetModuleMetaData](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getmodulemetadata-method.md) to obtain a metadata interface for a given module.</span></span> <span data-ttu-id="2901d-112">Le jeton de métadonnées qui est retourné à l'emplacement référencé par `pToken` peut alors servir à accéder aux métadonnées pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="2901d-112">The metadata token that is returned to the location referenced by `pToken` can then be used to access the metadata for the function.</span></span>  
  
 <span data-ttu-id="2901d-113">Le `ClassID` d’une fonction sur une classe générique peut ne pas être obtenu sans plus d’informations contextuelles sur l’utilisation de la fonction.</span><span class="sxs-lookup"><span data-stu-id="2901d-113">The `ClassID` of a function on a generic class might not be obtainable without more contextual information about the use of the function.</span></span> <span data-ttu-id="2901d-114">Dans ce cas, `pClassId` est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="2901d-114">In this case, `pClassId` will be 0.</span></span> <span data-ttu-id="2901d-115">Profiler le code doit utiliser [ICorProfilerInfo2::GetFunctionInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctioninfo2-method.md) avec la valeur COR_PRF_FRAME_INFO pour fournir plus de contexte.</span><span class="sxs-lookup"><span data-stu-id="2901d-115">Profiler code should use [ICorProfilerInfo2::GetFunctionInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctioninfo2-method.md) with a COR_PRF_FRAME_INFO value to provide more context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2901d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2901d-116">Requirements</span></span>  
 <span data-ttu-id="2901d-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2901d-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2901d-118">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2901d-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2901d-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2901d-119">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="2901d-120">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="2901d-120">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="2901d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2901d-121">See also</span></span>

- [<span data-ttu-id="2901d-122">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="2901d-122">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
