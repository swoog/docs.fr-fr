---
title: ICorProfilerInfo2::GetArrayObjectInfo, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetArrayObjectInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetArrayObjectInfo
helpviewer_keywords:
- ICorProfilerInfo2::GetArrayObjectInfo method [.NET Framework profiling]
- GetArrayObjectInfo method [.NET Framework profiling]
ms.assetid: bda75017-739f-4ce5-9000-f3b526e8473c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5276c69da05cedcd3195a09da12ddc5b2d0fed67
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59201271"
---
# <a name="icorprofilerinfo2getarrayobjectinfo-method"></a><span data-ttu-id="21bc6-102">ICorProfilerInfo2::GetArrayObjectInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="21bc6-102">ICorProfilerInfo2::GetArrayObjectInfo Method</span></span>
<span data-ttu-id="21bc6-103">Obtient des informations détaillées sur un objet tableau.</span><span class="sxs-lookup"><span data-stu-id="21bc6-103">Gets detailed information about an array object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21bc6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21bc6-104">Syntax</span></span>  
  
```  
HRESULT GetArrayObjectInfo(  
    [in] ObjectID objectId,  
    [in] ULONG32 cDimensions,  
    [out, size_is(cDimensions), length_is(cDimensions)] ULONG32 pDimensionSizes[],  
    [out, size_is(cDimensions), length_is(cDimensions)] int pDimensionLowerBounds[],  
    [out] BYTE **ppData);  
```  
  
## <a name="parameters"></a><span data-ttu-id="21bc6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21bc6-105">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="21bc6-106">[in] L’ID d’un objet de tableau valide.</span><span class="sxs-lookup"><span data-stu-id="21bc6-106">[in] The ID of a valid array object.</span></span>  
  
 `cDimensions`  
 <span data-ttu-id="21bc6-107">[in] Le rang (nombre de dimensions) du tableau.</span><span class="sxs-lookup"><span data-stu-id="21bc6-107">[in] The rank (number of dimensions) of the array.</span></span>  
  
 `pDimensionSizes`  
 <span data-ttu-id="21bc6-108">[out] Tableau qui contient des entiers, chacun représentant la taille d’une dimension du tableau.</span><span class="sxs-lookup"><span data-stu-id="21bc6-108">[out] An array that contains integers, each representing the size of a dimension of the array.</span></span>  
  
 `pDimensionLowerBounds`  
 <span data-ttu-id="21bc6-109">[out] Un tableau qui contient des entiers, chacun représentant faible lié d’une dimension du tableau.</span><span class="sxs-lookup"><span data-stu-id="21bc6-109">[out] An array that contains integers, each representing the lower bound of a dimension of the array.</span></span>  
  
 `ppData`  
 <span data-ttu-id="21bc6-110">[out] Un pointeur vers l’adresse de la mémoire tampon brute pour le tableau, ce qui est disposé en fonction de la C++ convention.</span><span class="sxs-lookup"><span data-stu-id="21bc6-110">[out] A pointer to the address of the raw buffer for the array, which is laid out according to the C++ convention.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="21bc6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="21bc6-111">Remarks</span></span>  
 <span data-ttu-id="21bc6-112">Le `pDimensionSizes` et `pDimensionLowerBounds` sont des tableaux parallèles, les éléments situés au même index dans chaque tableau sont des caractéristiques de la même entité.</span><span class="sxs-lookup"><span data-stu-id="21bc6-112">The `pDimensionSizes` and `pDimensionLowerBounds` are parallel arrays, so the elements located at the same index in each array are characteristics of the same entity.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="21bc6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21bc6-113">Requirements</span></span>  
 <span data-ttu-id="21bc6-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="21bc6-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="21bc6-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="21bc6-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="21bc6-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="21bc6-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="21bc6-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="21bc6-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21bc6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21bc6-118">See also</span></span>

- [<span data-ttu-id="21bc6-119">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="21bc6-119">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="21bc6-120">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="21bc6-120">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
