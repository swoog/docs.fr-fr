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
ms.openlocfilehash: 00a3afab4d5f6151bcd0efd2b658d4cd7fa8f1e0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33462200"
---
# <a name="icorprofilerinfogetilfunctionbodyallocator-method"></a><span data-ttu-id="78f91-102">ICorProfilerInfo::GetILFunctionBodyAllocator, méthode</span><span class="sxs-lookup"><span data-stu-id="78f91-102">ICorProfilerInfo::GetILFunctionBodyAllocator Method</span></span>
<span data-ttu-id="78f91-103">Obtient une interface qui fournit une méthode pour allouer de mémoire à utiliser pour permuter le corps d’une méthode dans le code Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="78f91-103">Gets an interface that provides a method to allocate memory to be used for swapping out the body of a method in Microsoft intermediate language (MSIL) code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="78f91-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78f91-104">Syntax</span></span>  
  
```  
HRESULT GetILFunctionBodyAllocator(  
    [in]  ModuleID      moduleId,  
    [out] IMethodMalloc **ppMalloc);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="78f91-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78f91-105">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="78f91-106">[in] L’ID du module dans lequel réside la méthode.</span><span class="sxs-lookup"><span data-stu-id="78f91-106">[in] The ID of the module in which the method resides.</span></span>  
  
 `ppMalloc`  
 <span data-ttu-id="78f91-107">[out] Un pointeur vers un [IMethodMalloc](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-interface.md) interface qui fournit une méthode pour allouer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="78f91-107">[out] A pointer to an [IMethodMalloc](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-interface.md) interface that provides a method to allocate the memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="78f91-108">Notes</span><span class="sxs-lookup"><span data-stu-id="78f91-108">Remarks</span></span>  
 <span data-ttu-id="78f91-109">Un corps de méthode dans du code MSIL doit être localisé comme une adresse virtuelle relative (RVA), relatif au module chargé, ce qui signifie qu’il suit le module de 4 Go.</span><span class="sxs-lookup"><span data-stu-id="78f91-109">A method body in MSIL code must be located as a relative virtual address (RVA), relative to the loaded module, which means that it follows the module within 4 GB.</span></span> <span data-ttu-id="78f91-110">Pour faciliter l’utilisation d’un outil permuter le corps d’une méthode, le `GetILFunctionBodyAllocator` méthode garantit que la mémoire est allouée dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="78f91-110">To make it easier for a tool to swap out the body of a method, the `GetILFunctionBodyAllocator` method ensures that memory is allocated within that range.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="78f91-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="78f91-111">Requirements</span></span>  
 <span data-ttu-id="78f91-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="78f91-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="78f91-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="78f91-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="78f91-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="78f91-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="78f91-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="78f91-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="78f91-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78f91-116">See Also</span></span>  
 [<span data-ttu-id="78f91-117">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="78f91-117">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
