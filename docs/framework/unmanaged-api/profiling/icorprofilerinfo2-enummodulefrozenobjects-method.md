---
title: ICorProfilerInfo2::EnumModuleFrozenObjects, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.EnumModuleFrozenObjects
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::EnumModuleFrozenObjects
helpviewer_keywords:
- EnumModuleFrozenObjects method [.NET Framework profiling]
- ICorProfilerInfo2::EnumModuleFrozenObjects method [.NET Framework profiling]
ms.assetid: 920b6483-7064-4d64-8613-fcc38ccf9b1e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a325c3e1aa9c08e00dc2cc38e3f7833fa9f99897
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57472575"
---
# <a name="icorprofilerinfo2enummodulefrozenobjects-method"></a><span data-ttu-id="debaa-102">ICorProfilerInfo2::EnumModuleFrozenObjects, méthode</span><span class="sxs-lookup"><span data-stu-id="debaa-102">ICorProfilerInfo2::EnumModuleFrozenObjects Method</span></span>
<span data-ttu-id="debaa-103">Obtient un énumérateur qui permet une itération sur les objets figés dans le module spécifié. Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="debaa-103">Gets an enumerator that allows iteration over the frozen objects in the specified module.This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="debaa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="debaa-104">Syntax</span></span>  
  
```  
HRESULT EnumModuleFrozenObjects(  
    [in] ModuleID moduleID,  
    [out] ICorProfilerObjectEnum** ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="debaa-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="debaa-105">Parameters</span></span>  
 `moduleID`  
 <span data-ttu-id="debaa-106">[in] L’ID du module qui contient les objets figés à énumérer.</span><span class="sxs-lookup"><span data-stu-id="debaa-106">[in] The ID of the module that contains the frozen objects to be enumerated.</span></span>  
  
 `ppEnum`  
 <span data-ttu-id="debaa-107">[out] Un pointeur vers l’adresse d’un [ICorProfilerObjectEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md) interface qui énumère les objets figés.</span><span class="sxs-lookup"><span data-stu-id="debaa-107">[out] A pointer to the address of an [ICorProfilerObjectEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md) interface, which enumerates the frozen objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="debaa-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="debaa-108">Requirements</span></span>  
 <span data-ttu-id="debaa-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="debaa-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="debaa-110">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="debaa-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="debaa-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="debaa-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="debaa-112">**Versions du .NET framework :** 3.5, 3.0 SP1, 3.0, 2.0 SP1, 2.0</span><span class="sxs-lookup"><span data-stu-id="debaa-112">**.NET Framework Versions:** 3.5, 3.0 SP1, 3.0, 2.0 SP1, 2.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="debaa-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="debaa-113">See also</span></span>
- [<span data-ttu-id="debaa-114">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="debaa-114">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="debaa-115">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="debaa-115">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
