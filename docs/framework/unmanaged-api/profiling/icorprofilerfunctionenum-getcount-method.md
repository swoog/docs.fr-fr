---
title: ICorProfilerFunctionEnum::GetCount, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionEnum.GetCount Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionEnum::GetCount
helpviewer_keywords:
- ICorProfilerFunctionEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerFunctionEnum interface [.NET Framework profiling]
ms.assetid: 62ec65e3-3e9d-400b-ae61-d24b8963995b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a5061750489c74e0385f2ce020c88518604b3167
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59169284"
---
# <a name="icorprofilerfunctionenumgetcount-method"></a><span data-ttu-id="c096d-102">ICorProfilerFunctionEnum::GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="c096d-102">ICorProfilerFunctionEnum::GetCount Method</span></span>
<span data-ttu-id="c096d-103">Obtient le nombre de fonctions qui ont été chargées par l'application ou chargées de force par le profileur.</span><span class="sxs-lookup"><span data-stu-id="c096d-103">Gets the number of functions that were loaded by the application or forcibly loaded by the profiler.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c096d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c096d-104">Syntax</span></span>  
  
```  
HRESULT GetCount([out] ULONG * pcelt);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c096d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c096d-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="c096d-106">[out] Le nombre de fonctions qui ont été chargées.</span><span class="sxs-lookup"><span data-stu-id="c096d-106">[out] The number of functions that were loaded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c096d-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c096d-107">Requirements</span></span>  
 <span data-ttu-id="c096d-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c096d-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c096d-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c096d-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c096d-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c096d-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c096d-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c096d-111">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c096d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c096d-112">See also</span></span>

- [<span data-ttu-id="c096d-113">ICorProfilerFunctionEnum, interface</span><span class="sxs-lookup"><span data-stu-id="c096d-113">ICorProfilerFunctionEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md)
- [<span data-ttu-id="c096d-114">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="c096d-114">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
