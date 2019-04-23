---
title: ICorProfilerInfo::GetILFunctionBodyAllocator, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetILFunctionBodyAllocator
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetILFunctionBodyAllocator
helpviewer_keywords:
- GetILFunctionBodyAllocator method [.NET Framework profiling]
- ICorProfilerInfo::GetILFunctionBodyAllocator method [.NET Framework profiling]
ms.assetid: 5da1bf3d-dddf-4892-b266-578ee54d570b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2cd66a895f99d62e8deaa45afab12d963aee2901
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59109120"
---
# <a name="icorprofilerinfogetilfunctionbodyallocator-method"></a><span data-ttu-id="f0a02-102">ICorProfilerInfo::GetILFunctionBodyAllocator, méthode</span><span class="sxs-lookup"><span data-stu-id="f0a02-102">ICorProfilerInfo::GetILFunctionBodyAllocator Method</span></span>
<span data-ttu-id="f0a02-103">Obtient une interface qui fournit une méthode pour allouer de mémoire pouvant être utilisée pour permuter le corps d’une méthode dans le code Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="f0a02-103">Gets an interface that provides a method to allocate memory to be used for swapping out the body of a method in Microsoft intermediate language (MSIL) code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0a02-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0a02-104">Syntax</span></span>  
  
```  
HRESULT GetILFunctionBodyAllocator(  
    [in]  ModuleID      moduleId,  
    [out] IMethodMalloc **ppMalloc);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f0a02-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0a02-105">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="f0a02-106">[in] L’ID du module dans lequel réside la méthode.</span><span class="sxs-lookup"><span data-stu-id="f0a02-106">[in] The ID of the module in which the method resides.</span></span>  
  
 `ppMalloc`  
 <span data-ttu-id="f0a02-107">[out] Un pointeur vers un [IMethodMalloc](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-interface.md) interface qui fournit une méthode pour allouer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f0a02-107">[out] A pointer to an [IMethodMalloc](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-interface.md) interface that provides a method to allocate the memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f0a02-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f0a02-108">Remarks</span></span>  
 <span data-ttu-id="f0a02-109">Un corps de méthode en code MSIL doit se trouver en tant qu’une adresse virtuelle relative (RVA), par rapport à module chargé, ce qui signifie qu’il suit le module au sein de 4 Go.</span><span class="sxs-lookup"><span data-stu-id="f0a02-109">A method body in MSIL code must be located as a relative virtual address (RVA), relative to the loaded module, which means that it follows the module within 4 GB.</span></span> <span data-ttu-id="f0a02-110">Pour faciliter un outil qui permet de permuter le corps d’une méthode, le `GetILFunctionBodyAllocator` méthode garantit que la mémoire est allouée dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="f0a02-110">To make it easier for a tool to swap out the body of a method, the `GetILFunctionBodyAllocator` method ensures that memory is allocated within that range.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0a02-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0a02-111">Requirements</span></span>  
 <span data-ttu-id="f0a02-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f0a02-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0a02-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="f0a02-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="f0a02-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f0a02-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f0a02-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0a02-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0a02-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0a02-116">See also</span></span>

- [<span data-ttu-id="f0a02-117">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="f0a02-117">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
