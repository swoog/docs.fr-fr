---
title: ICorProfilerInfo3::EnumModules, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.EnumModules Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::EnumModules
helpviewer_keywords:
- ICorProfilerInfo3::EnumModules method [.NET Framework profiling]
- EnumModules method [.NET Framework profiling]
ms.assetid: 1bf00b42-69da-4019-91b3-bf88026e83fb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: be5d05c34272b9fa5755b4d0e22fa9094707c5ec
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61703554"
---
# <a name="icorprofilerinfo3enummodules-method"></a><span data-ttu-id="79b09-102">ICorProfilerInfo3::EnumModules, méthode</span><span class="sxs-lookup"><span data-stu-id="79b09-102">ICorProfilerInfo3::EnumModules Method</span></span>
<span data-ttu-id="79b09-103">Retourne un énumérateur qui fournit des méthodes pour itérer séquentiellement au sein d’une collection de modules managés chargés dans l’application.</span><span class="sxs-lookup"><span data-stu-id="79b09-103">Returns an enumerator that provides methods to sequentially iterate through a collection of managed modules that are loaded into the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79b09-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79b09-104">Syntax</span></span>  
  
```  
HRESULT EnumModules([out] ICorProfilerModuleEnum** ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="79b09-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79b09-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="79b09-106">[out] Un pointeur vers un [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="79b09-106">[out] A pointer to an [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="79b09-107">Notes</span><span class="sxs-lookup"><span data-stu-id="79b09-107">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79b09-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79b09-108">Requirements</span></span>  
 <span data-ttu-id="79b09-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="79b09-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79b09-110">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="79b09-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="79b09-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="79b09-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="79b09-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79b09-112">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79b09-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79b09-113">See also</span></span>

- [<span data-ttu-id="79b09-114">ICorProfilerFunctionEnum, interface</span><span class="sxs-lookup"><span data-stu-id="79b09-114">ICorProfilerFunctionEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md)
- [<span data-ttu-id="79b09-115">ICorProfilerInfo3, interface</span><span class="sxs-lookup"><span data-stu-id="79b09-115">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [<span data-ttu-id="79b09-116">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="79b09-116">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="79b09-117">Profilage</span><span class="sxs-lookup"><span data-stu-id="79b09-117">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
