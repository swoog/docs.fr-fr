---
title: ICorProfilerModuleEnum::GetCount, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerModuleEnum.GetCount Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerModuleEnum::GetCount
helpviewer_keywords:
- ICorProfilerModuleEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerModuleEnum interface [.NET Framework profiling]
ms.assetid: f0a4a5e0-4689-474b-b0f4-37ca0639c918
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 91572887713216f94707e5d21e5767f4cc54e0d9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33456256"
---
# <a name="icorprofilermoduleenumgetcount-method"></a><span data-ttu-id="d71d3-102">ICorProfilerModuleEnum::GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="d71d3-102">ICorProfilerModuleEnum::GetCount Method</span></span>
<span data-ttu-id="d71d3-103">Obtient le nombre de modules managés chargés dans l'application.</span><span class="sxs-lookup"><span data-stu-id="d71d3-103">Gets the number of managed modules that were loaded into the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d71d3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d71d3-104">Syntax</span></span>  
  
```  
HRESULT GetCount([out] ULONG * pcelt);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d71d3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d71d3-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="d71d3-106">[out] Le nombre de modules du runtime dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d71d3-106">[out] The number of runtime modules in the collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d71d3-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d71d3-107">Requirements</span></span>  
 <span data-ttu-id="d71d3-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d71d3-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d71d3-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d71d3-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d71d3-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d71d3-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d71d3-111">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d71d3-111">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d71d3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d71d3-112">See Also</span></span>  
 [<span data-ttu-id="d71d3-113">ICorProfilerModuleEnum, interface</span><span class="sxs-lookup"><span data-stu-id="d71d3-113">ICorProfilerModuleEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md)  
 [<span data-ttu-id="d71d3-114">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="d71d3-114">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
