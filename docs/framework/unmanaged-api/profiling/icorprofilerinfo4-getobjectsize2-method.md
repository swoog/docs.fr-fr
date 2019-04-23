---
title: ICorProfilerInfo4::GetObjectSize2, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.GetObjectSize2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::GetObjectSize2
helpviewer_keywords:
- GetObjectSize2 method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::GetObjectSize2 method [.NET Framework profiling]
ms.assetid: 4a3e43ed-3ee3-4395-ab14-f78b903be13e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 15829e08a755b91ff91ca939b92a5a87bd377e8b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59176291"
---
# <a name="icorprofilerinfo4getobjectsize2-method"></a><span data-ttu-id="7b94b-102">ICorProfilerInfo4::GetObjectSize2, méthode</span><span class="sxs-lookup"><span data-stu-id="7b94b-102">ICorProfilerInfo4::GetObjectSize2 Method</span></span>
<span data-ttu-id="7b94b-103">Retourne la taille d’un objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="7b94b-103">Returns the size of a specified object.</span></span> <span data-ttu-id="7b94b-104">Remplace le [ICorProfilerInfo::GetObjectSize](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getobjectsize-method.md) méthode en signalant les tailles des objets supérieurs à ce qui peut être exprimé dans un `ULONG`.</span><span class="sxs-lookup"><span data-stu-id="7b94b-104">Replaces the [ICorProfilerInfo::GetObjectSize](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getobjectsize-method.md) method by reporting sizes of objects that are larger than what can be expressed in a `ULONG`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b94b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b94b-105">Syntax</span></span>  
  
```  
HRESULT GetObjectSize2(  
    [in]  ObjectID objectId,  
    [out] SIZE_T *pcSize);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7b94b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b94b-106">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="7b94b-107">[in] L’ID de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7b94b-107">[in] The ID of the object.</span></span>  
  
 `pcSize`  
 <span data-ttu-id="7b94b-108">[out] Pointeur vers la taille de l’objet, en octets.</span><span class="sxs-lookup"><span data-stu-id="7b94b-108">[out] A pointer to the object's size, in bytes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7b94b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="7b94b-109">Remarks</span></span>  
 <span data-ttu-id="7b94b-110">Différents objets des mêmes types ont souvent la même taille.</span><span class="sxs-lookup"><span data-stu-id="7b94b-110">Different objects of the same types often have the same size.</span></span> <span data-ttu-id="7b94b-111">Toutefois, certains types, tels que des tableaux ou des chaînes, peuvent avoir une taille différente pour chaque objet.</span><span class="sxs-lookup"><span data-stu-id="7b94b-111">However, some types, such as arrays or strings, may have a different size for each object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7b94b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b94b-112">Requirements</span></span>  
 <span data-ttu-id="7b94b-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7b94b-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7b94b-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7b94b-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7b94b-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7b94b-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7b94b-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7b94b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b94b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b94b-117">See also</span></span>

- [<span data-ttu-id="7b94b-118">ICorProfilerInfo4, interface</span><span class="sxs-lookup"><span data-stu-id="7b94b-118">ICorProfilerInfo4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)
