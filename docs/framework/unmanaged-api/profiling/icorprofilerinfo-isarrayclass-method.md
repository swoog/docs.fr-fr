---
title: ICorProfilerInfo::IsArrayClass, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.IsArrayClass
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::IsArrayClass
helpviewer_keywords:
- IsArrayClass method [.NET Framework profiling]
- ICorProfilerInfo::IsArrayClass method [.NET Framework profiling]
ms.assetid: 7f230961-23a6-4d56-ad2d-7a876d65705f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 350221ae205636cef82581f3fe11367006dd8b2b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59072170"
---
# <a name="icorprofilerinfoisarrayclass-method"></a><span data-ttu-id="8dc03-102">ICorProfilerInfo::IsArrayClass, méthode</span><span class="sxs-lookup"><span data-stu-id="8dc03-102">ICorProfilerInfo::IsArrayClass Method</span></span>
<span data-ttu-id="8dc03-103">Détermine si la classe spécifiée est une classe array.</span><span class="sxs-lookup"><span data-stu-id="8dc03-103">Determines whether the specified class is an array class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8dc03-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8dc03-104">Syntax</span></span>  
  
```  
HRESULT IsArrayClass(  
    [in]  ClassID        classId,  
    [out] CorElementType *pBaseElemType,  
    [out] ClassID        *pBaseClassId,  
    [out] ULONG          *pcRank);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8dc03-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8dc03-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="8dc03-106">[in] L’ID de la classe doit être examinée.</span><span class="sxs-lookup"><span data-stu-id="8dc03-106">[in] The ID of the class to be examined.</span></span>  
  
 `pBaseElemType`  
 <span data-ttu-id="8dc03-107">[out] Pointeur vers une valeur de l’énumération CorElementType qui indique le type des éléments du tableau.</span><span class="sxs-lookup"><span data-stu-id="8dc03-107">[out] A pointer to a value of the CorElementType enumeration that indicates the type of the array elements.</span></span>  
  
 `pBaseClassId`  
 <span data-ttu-id="8dc03-108">[out] Pointeur vers l’ID de classe des éléments du tableau, lorsqu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="8dc03-108">[out] A pointer to the class ID of the array elements, when available.</span></span>  
  
 `pcRank`  
 <span data-ttu-id="8dc03-109">[out] Pointeur vers un entier qui indique le classement (autrement dit, le nombre de dimensions) du tableau.</span><span class="sxs-lookup"><span data-stu-id="8dc03-109">[out] A pointer to an integer that indicates the rank (that is, number of dimensions) of the array.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8dc03-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8dc03-110">Remarks</span></span>  
 <span data-ttu-id="8dc03-111">Si la classe spécifiée est une classe array, la `IsArrayClass` méthode retourne une valeur S_OK HRESULT et des valeurs des paramètres de sortie non null.</span><span class="sxs-lookup"><span data-stu-id="8dc03-111">If the specified class is an array class, the `IsArrayClass` method returns an S_OK HRESULT and values for any non-null output parameters.</span></span> <span data-ttu-id="8dc03-112">Sinon, elle retourne S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="8dc03-112">Otherwise, it returns S_FALSE.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8dc03-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dc03-113">Requirements</span></span>  
 <span data-ttu-id="8dc03-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8dc03-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8dc03-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8dc03-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8dc03-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8dc03-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="8dc03-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="8dc03-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8dc03-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dc03-118">See also</span></span>

- [<span data-ttu-id="8dc03-119">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="8dc03-119">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
