---
title: ICorProfilerObjectEnum::Clone, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.Clone
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::Clone
helpviewer_keywords:
- Clone method, ICorProfilerObjectEnum interface [.NET Framework profiling]
- ICorProfilerObjectEnum::Clone method [.NET Framework profiling]
ms.assetid: b0b2facd-5991-4f4c-932d-c4937f45cef9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 14e8086532eff5dba6883575cc2daf447a32343a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59182362"
---
# <a name="icorprofilerobjectenumclone-method"></a><span data-ttu-id="eb775-102">ICorProfilerObjectEnum::Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="eb775-102">ICorProfilerObjectEnum::Clone Method</span></span>
<span data-ttu-id="eb775-103">Obtient un pointeur d’interface vers une copie de ce [ICorProfilerObjectEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="eb775-103">Gets an interface pointer to a copy of this [ICorProfilerObjectEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md) interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb775-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb775-104">Syntax</span></span>  
  
```  
HRESULT Clone (  
    [out] ICorProfilerObjectEnum   **ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eb775-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb775-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="eb775-106">[out] Un pointeur vers le pointeur d’interface qui pointe à son tour vers la copie de ce `ICorProfilerObjectEnum` interface.</span><span class="sxs-lookup"><span data-stu-id="eb775-106">[out] A pointer to the interface pointer that in turn points to the copy of this `ICorProfilerObjectEnum` interface.</span></span> <span data-ttu-id="eb775-107">La copie conserve son propre état d’énumération séparément à partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="eb775-107">The copy maintains its own enumeration state separately from this one.</span></span> <span data-ttu-id="eb775-108">Toutefois, position du curseur initiale de la copie sera identique à la position actuelle du curseur de cet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="eb775-108">However, the copy's initial cursor position will be the same as this enumerator's current cursor position.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb775-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb775-109">Requirements</span></span>  
 <span data-ttu-id="eb775-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eb775-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb775-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="eb775-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="eb775-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eb775-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="eb775-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="eb775-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="eb775-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb775-114">See also</span></span>

- [<span data-ttu-id="eb775-115">ICorProfilerObjectEnum, interface</span><span class="sxs-lookup"><span data-stu-id="eb775-115">ICorProfilerObjectEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md)
