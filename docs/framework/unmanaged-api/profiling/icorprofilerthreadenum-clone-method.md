---
title: ICorProfilerThreadEnum::Clone, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum.Clone
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum::Clone
helpviewer_keywords:
- Clone method, ICorProfilerThreadEnum interface [.NET Framework profiling]
- ICorProfilerThreadEnum::Clone method [.NET Framework profiling]
ms.assetid: 5a278bc9-88e2-4c69-b035-9d550dd77081
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0301334621a2e393a59e7cc34f2964450a81213f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59074168"
---
# <a name="icorprofilerthreadenumclone-method"></a><span data-ttu-id="fb6b4-102">ICorProfilerThreadEnum::Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="fb6b4-102">ICorProfilerThreadEnum::Clone Method</span></span>
<span data-ttu-id="fb6b4-103">Obtient un pointeur d’interface vers une copie de ce [ICorProfilerThreadEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="fb6b4-103">Gets an interface pointer to a copy of this [ICorProfilerThreadEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md) interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb6b4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb6b4-104">Syntax</span></span>  
  
```  
HRESULT Clone (    [out] ICorProfilerThreadEnum **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fb6b4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb6b4-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="fb6b4-106">[out] Un pointeur vers le pointeur d’interface, qui, à son tour, pointe vers la copie de ce [ICorProfilerThreadEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="fb6b4-106">[out] A pointer to the interface pointer, which, in turn, points to the copy of this [ICorProfilerThreadEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md) interface.</span></span> <span data-ttu-id="fb6b4-107">La copie de l’énumérateur maintient son propre état d’énumération séparément à partir de cet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="fb6b4-107">The copy of the enumerator maintains its own enumeration state separately from this enumerator.</span></span> <span data-ttu-id="fb6b4-108">Toutefois, la position du curseur initiale de la copie est identique à cette position actuelle du curseur de l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="fb6b4-108">However, the initial cursor position of the copy is the same as this current cursor position of the enumerator.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fb6b4-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb6b4-109">Requirements</span></span>  
 <span data-ttu-id="fb6b4-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fb6b4-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fb6b4-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fb6b4-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fb6b4-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fb6b4-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="fb6b4-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="fb6b4-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="fb6b4-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb6b4-114">See also</span></span>

- [<span data-ttu-id="fb6b4-115">ICorProfilerThreadEnum</span><span class="sxs-lookup"><span data-stu-id="fb6b4-115">ICorProfilerThreadEnum</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="fb6b4-116">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="fb6b4-116">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
