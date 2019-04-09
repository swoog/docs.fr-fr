---
title: ICorProfilerFunctionEnum::Clone, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionEnum.Clone Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionEnum::Clone
helpviewer_keywords:
- ICorProfilerFunctionEnum::Clone method [.NET Framework profiling]
- Clone method, ICorProfilerFunctionEnum interface [.NET Framework profiling]
ms.assetid: 0c3d4835-e111-4e82-af6d-53f140b8f2c9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5ffd1fcc36f0c6cc3c5f063c5a916e8918839566
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59135588"
---
# <a name="icorprofilerfunctionenumclone-method"></a><span data-ttu-id="fefd3-102">ICorProfilerFunctionEnum::Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="fefd3-102">ICorProfilerFunctionEnum::Clone Method</span></span>
<span data-ttu-id="fefd3-103">Obtient un pointeur d’interface vers une copie de ce [ICorProfilerFunctionEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="fefd3-103">Gets an interface pointer to a copy of this [ICorProfilerFunctionEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md) interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fefd3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fefd3-104">Syntax</span></span>  
  
```  
HRESULT Clone([out] ICorProfilerFunctionEnum **ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fefd3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fefd3-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="fefd3-106">[out] Un pointeur vers le pointeur d’interface, qui, à son tour, pointe vers la copie de ce [ICorProfilerFunctionEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="fefd3-106">[out] A pointer to the interface pointer, which, in turn, points to the copy of this [ICorProfilerFunctionEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md) interface.</span></span> <span data-ttu-id="fefd3-107">La copie de l’énumérateur maintient son propre état d’énumération séparément à partir de cet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="fefd3-107">The copy of the enumerator maintains its own enumeration state separately from this enumerator.</span></span> <span data-ttu-id="fefd3-108">Toutefois, la position du curseur initiale de la copie est identique à la position actuelle du curseur de cet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="fefd3-108">However, the copy's initial cursor position is the same as this enumerator's current cursor position.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fefd3-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fefd3-109">Requirements</span></span>  
 <span data-ttu-id="fefd3-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fefd3-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fefd3-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fefd3-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fefd3-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fefd3-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="fefd3-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="fefd3-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="fefd3-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fefd3-114">See also</span></span>

- [<span data-ttu-id="fefd3-115">ICorProfilerFunctionEnum, interface</span><span class="sxs-lookup"><span data-stu-id="fefd3-115">ICorProfilerFunctionEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md)
- [<span data-ttu-id="fefd3-116">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="fefd3-116">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
