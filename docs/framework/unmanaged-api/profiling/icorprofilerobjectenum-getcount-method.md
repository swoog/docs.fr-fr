---
title: ICorProfilerObjectEnum::GetCount, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.GetCount
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::GetCount
helpviewer_keywords:
- ICorProfilerObjectEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerObjectEnum interface [.NET Framework profiling]
ms.assetid: 166b0761-ed80-4ccd-9973-dc20e61bf8fa
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a363021700eacea1d4af80ca6371de5c587afda1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54622199"
---
# <a name="icorprofilerobjectenumgetcount-method"></a><span data-ttu-id="178fa-102">ICorProfilerObjectEnum::GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="178fa-102">ICorProfilerObjectEnum::GetCount Method</span></span>
<span data-ttu-id="178fa-103">Obtient le nombre total d’objets figés dans la collection.</span><span class="sxs-lookup"><span data-stu-id="178fa-103">Gets the total number of frozen objects in the collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="178fa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="178fa-104">Syntax</span></span>  
  
```  
HRESULT GetCount (  
    [out] ULONG   *pcelt  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="178fa-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="178fa-105">Parameters</span></span>  
 `pcelt`  
 <span data-ttu-id="178fa-106">[out] Pointeur vers le nombre d’objets figés dans la collection.</span><span class="sxs-lookup"><span data-stu-id="178fa-106">[out] A pointer to the number of frozen objects in the collection.</span></span>  
  
 <span data-ttu-id="178fa-107">Cette méthode retourne toujours zéro dans le .NET Framework version 3.5 Service Pack 1 (SP1) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="178fa-107">This method will always return zero in the .NET Framework version 3.5 Service Pack 1 (SP1) and later versions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="178fa-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="178fa-108">Requirements</span></span>  
 <span data-ttu-id="178fa-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="178fa-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="178fa-110">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="178fa-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="178fa-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="178fa-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="178fa-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="178fa-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="178fa-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="178fa-113">See also</span></span>
- [<span data-ttu-id="178fa-114">ICorProfilerObjectEnum, interface</span><span class="sxs-lookup"><span data-stu-id="178fa-114">ICorProfilerObjectEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md)
