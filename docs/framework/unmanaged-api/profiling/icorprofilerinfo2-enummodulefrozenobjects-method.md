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
ms.openlocfilehash: 77b07dae5b53db58b3628f677be1714e66ac18ad
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455255"
---
# <a name="icorprofilerinfo2enummodulefrozenobjects-method"></a><span data-ttu-id="b118b-102">ICorProfilerInfo2::EnumModuleFrozenObjects, méthode</span><span class="sxs-lookup"><span data-stu-id="b118b-102">ICorProfilerInfo2::EnumModuleFrozenObjects Method</span></span>
<span data-ttu-id="b118b-103">Obtient un énumérateur qui permet l’itération sur les objets figés dans le module spécifié. Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="b118b-103">Gets an enumerator that allows iteration over the frozen objects in the specified module.This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b118b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b118b-104">Syntax</span></span>  
  
```  
HRESULT EnumModuleFrozenObjects(  
    [in] ModuleID moduleID,  
    [out] ICorProfilerObjectEnum** ppEnum);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b118b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b118b-105">Parameters</span></span>  
 `moduleID`  
 <span data-ttu-id="b118b-106">[in] L’ID du module qui contient les objets figés à énumérer.</span><span class="sxs-lookup"><span data-stu-id="b118b-106">[in] The ID of the module that contains the frozen objects to be enumerated.</span></span>  
  
 `ppEnum`  
 <span data-ttu-id="b118b-107">[out] Un pointeur vers l’adresse d’un [ICorProfilerObjectEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md) interface qui énumère les objets figés.</span><span class="sxs-lookup"><span data-stu-id="b118b-107">[out] A pointer to the address of an [ICorProfilerObjectEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md) interface, which enumerates the frozen objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b118b-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b118b-108">Requirements</span></span>  
 <span data-ttu-id="b118b-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b118b-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b118b-110">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b118b-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b118b-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b118b-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b118b-112">**Versions du .NET framework :** 3.5, 3.0 SP1, 3.0, 2.0 SP1, 2.0</span><span class="sxs-lookup"><span data-stu-id="b118b-112">**.NET Framework Versions:** 3.5, 3.0 SP1, 3.0, 2.0 SP1, 2.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b118b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b118b-113">See Also</span></span>  
 [<span data-ttu-id="b118b-114">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="b118b-114">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="b118b-115">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="b118b-115">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
