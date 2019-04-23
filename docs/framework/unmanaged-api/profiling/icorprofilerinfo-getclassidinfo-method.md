---
title: ICorProfilerInfo::GetClassIDInfo, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetClassIDInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetClassIDInfo
helpviewer_keywords:
- GetClassIDInfo method [.NET Framework profiling]
- ICorProfilerInfo::GetClassIDInfo method [.NET Framework profiling]
ms.assetid: 9e93b99e-5aca-415c-8e37-7f33753b612d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 45abb39fa7266e19bbd375b476f2ab48bfc5914d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59129998"
---
# <a name="icorprofilerinfogetclassidinfo-method"></a><span data-ttu-id="d7935-102">ICorProfilerInfo::GetClassIDInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="d7935-102">ICorProfilerInfo::GetClassIDInfo Method</span></span>
<span data-ttu-id="d7935-103">Obtient le module parent et le jeton de métadonnées pour la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d7935-103">Gets the parent module and the metadata token for the specified class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d7935-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7935-104">Syntax</span></span>  
  
```  
HRESULT GetClassIDInfo(  
    [in]  ClassID   classId,  
    [out] ModuleID  *pModuleId,  
    [out] mdTypeDef *pTypeDefToken);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d7935-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7935-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="d7935-106">[in] L’ID de la classe pour laquelle obtenir les informations.</span><span class="sxs-lookup"><span data-stu-id="d7935-106">[in] The ID of the class for which to get the information.</span></span>  
  
 `pModuleId`  
 <span data-ttu-id="d7935-107">[out] Un pointeur vers l’ID du module parent de la classe.</span><span class="sxs-lookup"><span data-stu-id="d7935-107">[out] A pointer to the ID of the parent module of the class.</span></span>  
  
 `pTypeDefToken`  
 <span data-ttu-id="d7935-108">[out] Pointeur vers le jeton de métadonnées pour la classe.</span><span class="sxs-lookup"><span data-stu-id="d7935-108">[out] A pointer to the metadata token for the class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d7935-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d7935-109">Remarks</span></span>  
 <span data-ttu-id="d7935-110">Le code de profileur peut appeler [ICorProfilerInfo::GetModuleMetaData](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getmodulemetadata-method.md) pour obtenir une interface de métadonnées pour un module donné.</span><span class="sxs-lookup"><span data-stu-id="d7935-110">The profiler code can call [ICorProfilerInfo::GetModuleMetaData](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getmodulemetadata-method.md) to obtain a metadata interface for a given module.</span></span> <span data-ttu-id="d7935-111">Le jeton de métadonnées qui est retourné à l'emplacement référencé par `pTypeDefToken` peut alors servir à accéder aux métadonnées pour la classe.</span><span class="sxs-lookup"><span data-stu-id="d7935-111">The metadata token that is returned to the location referenced by `pTypeDefToken` can then be used to access the metadata for the class.</span></span>  
  
 <span data-ttu-id="d7935-112">Pour obtenir plus d’informations pour les types génériques, utilisez [ICorProfilerInfo2::GetClassIDInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getclassidinfo2-method.md).</span><span class="sxs-lookup"><span data-stu-id="d7935-112">To get more information for generic types, use [ICorProfilerInfo2::GetClassIDInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getclassidinfo2-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d7935-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7935-113">Requirements</span></span>  
 <span data-ttu-id="d7935-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d7935-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d7935-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d7935-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d7935-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d7935-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d7935-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d7935-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d7935-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7935-118">See also</span></span>

- [<span data-ttu-id="d7935-119">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="d7935-119">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
