---
title: ICorProfilerModuleEnum::Skip, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerModuleEnum.Skip Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerModuleEnum::Skip
helpviewer_keywords:
- Skip method, ICorProfilerModuleEnum interface [.NET Framework profiling]
- ICorProfilerModuleEnum::Skip method [.NET Framework profiling]
ms.assetid: 8dc29c6a-e2ba-41d8-a1e0-0fdd21421e0b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 397e8afcc176bcd9733e83dc6425fe49f385931e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59078200"
---
# <a name="icorprofilermoduleenumskip-method"></a><span data-ttu-id="21582-102">ICorProfilerModuleEnum::Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="21582-102">ICorProfilerModuleEnum::Skip Method</span></span>
<span data-ttu-id="21582-103">Fait avancer le curseur de l'énumérateur depuis sa position actuelle de manière à ignorer le nombre spécifié d'éléments.</span><span class="sxs-lookup"><span data-stu-id="21582-103">Advances the enumerator's cursor from its current position so that the specified number of elements are skipped.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21582-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21582-104">Syntax</span></span>  
  
```  
HRESULT Skip([in] ULONG celt);  
```  
  
## <a name="parameters"></a><span data-ttu-id="21582-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21582-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="21582-106">[in] Le nombre d’éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="21582-106">[in] The number of elements to be skipped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="21582-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="21582-107">Return Value</span></span>  
 <span data-ttu-id="21582-108">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="21582-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="21582-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="21582-109">HRESULT</span></span>|<span data-ttu-id="21582-110">Description</span><span class="sxs-lookup"><span data-stu-id="21582-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="21582-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="21582-111">S_OK</span></span>|<span data-ttu-id="21582-112">`celt` éléments ont été ignorés.</span><span class="sxs-lookup"><span data-stu-id="21582-112">`celt` elements were skipped.</span></span>|  
|<span data-ttu-id="21582-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="21582-113">S_FALSE</span></span>|<span data-ttu-id="21582-114">Moins de `celt` éléments ont été ignorés, ce qui indique qu’il n’y a aucun autre élément.</span><span class="sxs-lookup"><span data-stu-id="21582-114">Fewer than `celt` elements were skipped, which indicates that there are no more elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="21582-115">Notes</span><span class="sxs-lookup"><span data-stu-id="21582-115">Remarks</span></span>  
 <span data-ttu-id="21582-116">La nouvelle position du curseur de cet énumérateur est (position actuelle) + `celt`.</span><span class="sxs-lookup"><span data-stu-id="21582-116">The new position of this enumerator's cursor is (current position) + `celt`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="21582-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21582-117">Requirements</span></span>  
 <span data-ttu-id="21582-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="21582-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="21582-119">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="21582-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="21582-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="21582-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="21582-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="21582-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21582-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21582-122">See also</span></span>

- [<span data-ttu-id="21582-123">ICorProfilerModuleEnum, interface</span><span class="sxs-lookup"><span data-stu-id="21582-123">ICorProfilerModuleEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md)
- [<span data-ttu-id="21582-124">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="21582-124">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
