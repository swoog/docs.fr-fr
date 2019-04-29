---
title: ICorProfilerInfo7::GetInMemorySymbolsLength (méthode)
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo7.GetInMemorySymbolsLength
api_location:
- mscorwks.dll
- icorprof.idl
api_type:
- COM
ms.assetid: d62c4a4c-8a62-45aa-8f01-a8387cf36159
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 422fdfef6bea40e0f4bcc7447df8dba1eab2896e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61919085"
---
# <a name="icorprofilerinfo7getinmemorysymbolslength-method"></a><span data-ttu-id="fe47f-102">ICorProfilerInfo7::GetInMemorySymbolsLength (méthode)</span><span class="sxs-lookup"><span data-stu-id="fe47f-102">ICorProfilerInfo7::GetInMemorySymbolsLength Method</span></span>
<span data-ttu-id="fe47f-103">[Prise en charge dans le .NET Framework 4.6.1 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="fe47f-103">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="fe47f-104">Retourne la longueur d’un flux de symbole d’en mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe47f-104">Returns the length of an in-memory symbol stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe47f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe47f-105">Syntax</span></span>  
  
```  
HRESULT GetInMemorySymbolsLength(  
        [in] ModuleID moduleId,  
        [out] DWORD* pCountSymbolBytes  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fe47f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe47f-106">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="fe47f-107">[in] L’identificateur du module qui contient le flux en mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe47f-107">[in] The identifier of the module containing the in-memory stream.</span></span>  
  
 <span data-ttu-id="fe47f-108">pCountSymbolBytes</span><span class="sxs-lookup"><span data-stu-id="fe47f-108">pCountSymbolBytes</span></span>  
 <span data-ttu-id="fe47f-109">[out] Un pointeur vers un `DWORD` valeur qui, lorsque la méthode est retournée, contient la longueur du flux en octets.</span><span class="sxs-lookup"><span data-stu-id="fe47f-109">[out] A pointer to a `DWORD` value that, when the method returns, contains the length of the stream in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fe47f-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fe47f-110">Return Value</span></span>  
 <span data-ttu-id="fe47f-111">La méthode retourne `S_OK` si la longueur du flux de mémoire peut être déterminée, même si elle est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="fe47f-111">The method returns `S_OK` if the length of the memory stream can be determined, even if it is zero (0).</span></span>  
  
 <span data-ttu-id="fe47f-112">La méthode retourne `CORPROF_E_MODULE_IS_DYNAMIC` si la méthode a été créée à l’aide de <xref:System.Reflection.Emit?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="fe47f-112">The method returns `CORPROF_E_MODULE_IS_DYNAMIC` if the method was created using <xref:System.Reflection.Emit?displayProperty=nameWithType>.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fe47f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="fe47f-113">Remarks</span></span>  
 <span data-ttu-id="fe47f-114">Si le module a de symboles en mémoire, la longueur du flux de données est placée dans `pCountSymbolBytes`.</span><span class="sxs-lookup"><span data-stu-id="fe47f-114">If the module has in-memory symbols, the length of the stream is placed in `pCountSymbolBytes`.</span></span> <span data-ttu-id="fe47f-115">Si le module n’a pas les symboles en mémoire, `*pCountSymbolBytes = 0`.</span><span class="sxs-lookup"><span data-stu-id="fe47f-115">If the module doesn't have in-memory     symbols, `*pCountSymbolBytes = 0`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fe47f-116">L’implémentation actuelle ne prend pas en charge de Reflection.Emit.</span><span class="sxs-lookup"><span data-stu-id="fe47f-116">The current implementation does not support Reflection.Emit.</span></span> <span data-ttu-id="fe47f-117">Si le module a été créé à l’aide de Reflection.Emit, la méthode retourne `CORPROF_E_MODULE_IS_DYNAMIC`.</span><span class="sxs-lookup"><span data-stu-id="fe47f-117">If the module was created by using Reflection.Emit, the method returns `CORPROF_E_MODULE_IS_DYNAMIC`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe47f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe47f-118">Requirements</span></span>  
 <span data-ttu-id="fe47f-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fe47f-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe47f-120">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fe47f-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fe47f-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fe47f-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fe47f-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe47f-122">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe47f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe47f-123">See also</span></span>

- [<span data-ttu-id="fe47f-124">ICorProfilerInfo7, interface</span><span class="sxs-lookup"><span data-stu-id="fe47f-124">ICorProfilerInfo7 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-interface.md)
