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
ms.openlocfilehash: cce96e8c6d046beba9e45c7121bf68444fd51c95
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61597953"
---
# <a name="icorprofilerthreadenumskip-method"></a><span data-ttu-id="c796b-102">ICorProfilerThreadEnum::Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="c796b-102">ICorProfilerThreadEnum::Skip Method</span></span>
<span data-ttu-id="c796b-103">Fait avancer le curseur de l'énumérateur depuis sa position actuelle de manière à ignorer le nombre spécifié d'éléments.</span><span class="sxs-lookup"><span data-stu-id="c796b-103">Advances the enumerator's cursor from its current position to skip the specified number of elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c796b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c796b-104">Syntax</span></span>  
  
```  
HRESULT Skip (    [in] ULONG celt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c796b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c796b-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="c796b-106">[in] Le nombre d’éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="c796b-106">[in] The number of elements to be skipped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c796b-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c796b-107">Return Value</span></span>  
 <span data-ttu-id="c796b-108">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="c796b-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="c796b-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c796b-109">HRESULT</span></span>|<span data-ttu-id="c796b-110">Description</span><span class="sxs-lookup"><span data-stu-id="c796b-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c796b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="c796b-111">S_OK</span></span>|<span data-ttu-id="c796b-112">`celt` éléments ont été ignorés.</span><span class="sxs-lookup"><span data-stu-id="c796b-112">`celt` elements were skipped.</span></span>|  
|<span data-ttu-id="c796b-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="c796b-113">S_FALSE</span></span>|<span data-ttu-id="c796b-114">Moins de `celt` éléments ont été ignorés, ce qui indique qu’il n’y a aucun autre élément.</span><span class="sxs-lookup"><span data-stu-id="c796b-114">Fewer than `celt` elements were skipped, which indicates that there are no more elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c796b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c796b-115">Remarks</span></span>  
 <span data-ttu-id="c796b-116">La nouvelle position du curseur de cet énumérateur est (position actuelle) + `celt`.</span><span class="sxs-lookup"><span data-stu-id="c796b-116">The new position of this enumerator's cursor is (current position) + `celt`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c796b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c796b-117">Requirements</span></span>  
 <span data-ttu-id="c796b-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c796b-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c796b-119">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c796b-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c796b-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c796b-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c796b-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c796b-121">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c796b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c796b-122">See also</span></span>

- [<span data-ttu-id="c796b-123">ICorProfilerThreadEnum, interface</span><span class="sxs-lookup"><span data-stu-id="c796b-123">ICorProfilerThreadEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="c796b-124">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="c796b-124">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
