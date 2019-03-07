---
title: ICorProfilerObjectEnum::Skip, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.Skip
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::Skip
helpviewer_keywords:
- ICorProfilerObjectEnum::Skip method [.NET Framework profiling]
- Skip method, ICorProfilerObjectEnum interface [.NET Framework profiling]
ms.assetid: f8e498f8-f93a-4b82-bd22-55bdbf5e8d45
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a7d1273c51dcfb63e3671b7b9d893e1022d55247
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57473070"
---
# <a name="icorprofilerobjectenumskip-method"></a><span data-ttu-id="150a6-102">ICorProfilerObjectEnum::Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="150a6-102">ICorProfilerObjectEnum::Skip Method</span></span>
<span data-ttu-id="150a6-103">Avance le curseur de cet énumérateur depuis sa position actuelle afin que le nombre spécifié d’éléments soit ignoré.</span><span class="sxs-lookup"><span data-stu-id="150a6-103">Advances the cursor of this enumerator from its current position so that the specified number of elements are skipped.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="150a6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="150a6-104">Syntax</span></span>  
  
```  
HRESULT Skip (  
    [in] ULONG   celt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="150a6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="150a6-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="150a6-106">[in] Le nombre d’éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="150a6-106">[in] The number of elements to be skipped.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="150a6-107">Notes</span><span class="sxs-lookup"><span data-stu-id="150a6-107">Remarks</span></span>  
 <span data-ttu-id="150a6-108">La nouvelle position du curseur de cet énumérateur est : (position actuelle) + `celt` .</span><span class="sxs-lookup"><span data-stu-id="150a6-108">The new position of this enumerator's cursor is: (current position) + `celt` .</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="150a6-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="150a6-109">Requirements</span></span>  
 <span data-ttu-id="150a6-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="150a6-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="150a6-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="150a6-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="150a6-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="150a6-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="150a6-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="150a6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="150a6-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="150a6-114">See also</span></span>
- [<span data-ttu-id="150a6-115">ICorProfilerObjectEnum, interface</span><span class="sxs-lookup"><span data-stu-id="150a6-115">ICorProfilerObjectEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md)
