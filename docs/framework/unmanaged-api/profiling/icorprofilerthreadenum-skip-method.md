---
title: ICorProfilerThreadEnum::Skip, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum.Skip
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum::Skip
helpviewer_keywords:
- Skip method, ICorProfilerThreadEnum interface [.NET Framework profiling]
- ICorProfilerThreadEnum::Skip method [.NET Framework profiling]
ms.assetid: acb8b029-4a96-4ed7-ae3c-310204e5ceea
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: af6aab2483f0e92dc20936fe2b01e12590d99ca7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455368"
---
# <a name="icorprofilerthreadenumskip-method"></a><span data-ttu-id="9e10e-102">ICorProfilerThreadEnum::Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="9e10e-102">ICorProfilerThreadEnum::Skip Method</span></span>
<span data-ttu-id="9e10e-103">Fait avancer le curseur de l'énumérateur depuis sa position actuelle de manière à ignorer le nombre spécifié d'éléments.</span><span class="sxs-lookup"><span data-stu-id="9e10e-103">Advances the enumerator's cursor from its current position to skip the specified number of elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e10e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e10e-104">Syntax</span></span>  
  
```  
HRESULT Skip (    [in] ULONG celt  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9e10e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e10e-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="9e10e-106">[in] Le nombre d’éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="9e10e-106">[in] The number of elements to be skipped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9e10e-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9e10e-107">Return Value</span></span>  
 <span data-ttu-id="9e10e-108">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="9e10e-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="9e10e-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9e10e-109">HRESULT</span></span>|<span data-ttu-id="9e10e-110">Description</span><span class="sxs-lookup"><span data-stu-id="9e10e-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9e10e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e10e-111">S_OK</span></span>|<span data-ttu-id="9e10e-112">`celt` éléments ont été ignorés.</span><span class="sxs-lookup"><span data-stu-id="9e10e-112">`celt` elements were skipped.</span></span>|  
|<span data-ttu-id="9e10e-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="9e10e-113">S_FALSE</span></span>|<span data-ttu-id="9e10e-114">Moins de `celt` éléments ont été ignorés, ce qui signifie qu’il n’y a plus d’éléments.</span><span class="sxs-lookup"><span data-stu-id="9e10e-114">Fewer than `celt` elements were skipped, which indicates that there are no more elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9e10e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9e10e-115">Remarks</span></span>  
 <span data-ttu-id="9e10e-116">La nouvelle position du curseur de cet énumérateur est (position actuelle) + `celt`.</span><span class="sxs-lookup"><span data-stu-id="9e10e-116">The new position of this enumerator's cursor is (current position) + `celt`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9e10e-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9e10e-117">Requirements</span></span>  
 <span data-ttu-id="9e10e-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9e10e-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9e10e-119">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="9e10e-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="9e10e-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9e10e-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9e10e-121">**Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9e10e-121">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9e10e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e10e-122">See Also</span></span>  
 [<span data-ttu-id="9e10e-123">ICorProfilerThreadEnum, interface</span><span class="sxs-lookup"><span data-stu-id="9e10e-123">ICorProfilerThreadEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md)  
 [<span data-ttu-id="9e10e-124">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="9e10e-124">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
