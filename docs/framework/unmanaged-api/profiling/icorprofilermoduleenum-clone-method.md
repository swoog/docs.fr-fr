---
title: ICorProfilerModuleEnum::Clone, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerModuleEnum.Clone Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerModuleEnum::Clone
helpviewer_keywords:
- Clone method, ICorProfilerModuleEnum interface [.NET Framework profiling]
- ICorProfilerModuleEnum::Clone method [.NET Framework profiling]
ms.assetid: 7dec7e36-8d88-416d-b437-abf98b76c1df
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9249e6f5ee7b15d55f5518263b0ac2e31b64e993
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33454458"
---
# <a name="icorprofilermoduleenumclone-method"></a><span data-ttu-id="ae0f6-102">ICorProfilerModuleEnum::Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="ae0f6-102">ICorProfilerModuleEnum::Clone Method</span></span>
<span data-ttu-id="ae0f6-103">Obtient un pointeur d’interface vers une copie de cette [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="ae0f6-103">Gets an interface pointer to a copy of this [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae0f6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae0f6-104">Syntax</span></span>  
  
```  
HRESULT Clone([out] ICorProfilerObjectEnum **ppEnum);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ae0f6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae0f6-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="ae0f6-106">[out] Un pointeur vers le pointeur d’interface qui pointe à son tour vers la copie de cette [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="ae0f6-106">[out] A pointer to the interface pointer that in turn points to the copy of this [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) interface.</span></span> <span data-ttu-id="ae0f6-107">La copie de l’énumérateur maintient son propre état d’énumération séparément à partir de cet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="ae0f6-107">The copy of the enumerator maintains its own enumeration state separately from this enumerator.</span></span> <span data-ttu-id="ae0f6-108">Toutefois, la position du curseur initiale de la copie est identique à la position actuelle du curseur de cet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="ae0f6-108">However, the copy's initial cursor position is the same as this enumerator's current cursor position.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae0f6-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ae0f6-109">Requirements</span></span>  
 <span data-ttu-id="ae0f6-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ae0f6-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae0f6-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ae0f6-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ae0f6-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ae0f6-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ae0f6-113">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae0f6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae0f6-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae0f6-114">See Also</span></span>  
 [<span data-ttu-id="ae0f6-115">ICorProfilerModuleEnum, interface</span><span class="sxs-lookup"><span data-stu-id="ae0f6-115">ICorProfilerModuleEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md)  
 [<span data-ttu-id="ae0f6-116">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="ae0f6-116">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
