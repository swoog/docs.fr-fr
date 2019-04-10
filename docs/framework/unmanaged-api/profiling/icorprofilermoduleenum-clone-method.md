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
ms.openlocfilehash: 9053505f7356f4618993ead911f730909f53f383
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59227143"
---
# <a name="icorprofilermoduleenumclone-method"></a><span data-ttu-id="56814-102">ICorProfilerModuleEnum::Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="56814-102">ICorProfilerModuleEnum::Clone Method</span></span>
<span data-ttu-id="56814-103">Obtient un pointeur d’interface vers une copie de ce [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="56814-103">Gets an interface pointer to a copy of this [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="56814-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56814-104">Syntax</span></span>  
  
```  
HRESULT Clone([out] ICorProfilerObjectEnum **ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="56814-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56814-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="56814-106">[out] Un pointeur vers le pointeur d’interface qui pointe à son tour vers la copie de ce [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="56814-106">[out] A pointer to the interface pointer that in turn points to the copy of this [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) interface.</span></span> <span data-ttu-id="56814-107">La copie de l’énumérateur maintient son propre état d’énumération séparément à partir de cet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="56814-107">The copy of the enumerator maintains its own enumeration state separately from this enumerator.</span></span> <span data-ttu-id="56814-108">Toutefois, la position du curseur initiale de la copie est identique à la position actuelle du curseur de cet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="56814-108">However, the copy's initial cursor position is the same as this enumerator's current cursor position.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="56814-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56814-109">Requirements</span></span>  
 <span data-ttu-id="56814-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="56814-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="56814-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="56814-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="56814-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="56814-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="56814-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="56814-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="56814-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56814-114">See also</span></span>

- [<span data-ttu-id="56814-115">ICorProfilerModuleEnum, interface</span><span class="sxs-lookup"><span data-stu-id="56814-115">ICorProfilerModuleEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md)
- [<span data-ttu-id="56814-116">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="56814-116">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
