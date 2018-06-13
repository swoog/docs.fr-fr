---
title: ICorProfilerInfo3::GetFunctionEnter3Info, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.GetFunctionEnter3Info Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::GetFunctionEnter3Info
helpviewer_keywords:
- GetFunctionEnter3Info method [.NET Framework profiling]
- ICorProfilerInfo3::GetFunctionEnter3Info method [.NET Framework profiling]
ms.assetid: 542c7c65-dd56-4651-b76f-5db2465e4a15
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e5d06988330b9ec83463165661ea5425d8563c60
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33459053"
---
# <a name="icorprofilerinfo3getfunctionenter3info-method"></a><span data-ttu-id="f1cc3-102">ICorProfilerInfo3::GetFunctionEnter3Info, méthode</span><span class="sxs-lookup"><span data-stu-id="f1cc3-102">ICorProfilerInfo3::GetFunctionEnter3Info Method</span></span>
<span data-ttu-id="f1cc3-103">Fournit les informations de frame et d’arguments de pile de la fonction signalée au profileur par la [FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="f1cc3-103">Provides the stack frame and argument information of the function that is being reported to the profiler by the [FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md) function.</span></span> <span data-ttu-id="f1cc3-104">Cette méthode peut être appelée uniquement pendant le rappel de `FunctionEnter3WithInfo`.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-104">This method can be called only during the `FunctionEnter3WithInfo` callback.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1cc3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1cc3-105">Syntax</span></span>  
  
```  
HRESULT GetFunctionEnter3Info(  
            [in]  FunctionID functionId,   
            [in]  COR_PRF_ELT_INFO eltInfo,  
            [out] COR_PRF_FRAME_INFO *pFrameInfo,  
            [in, out] ULONG *pcbArgumentInfo,  
            [out, size_is(*pcbArgumentInfo)]  
                  COR_PRF_FUNCTION_ARGUMENT_INFO *pArgumentInfo);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f1cc3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1cc3-106">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="f1cc3-107">[in] `FunctionID` de la fonction entrée.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-107">[in] The `FunctionID` of the function that is being entered.</span></span>  
  
 `eltInfo`  
 <span data-ttu-id="f1cc3-108">[in] Handle opaque qui représente des informations sur un frame de pile donné.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-108">[in] An opaque handle that represents information about a given stack frame.</span></span> <span data-ttu-id="f1cc3-109">Le profileur doit fournir les mêmes `eltInfo` qui lui a été attribué par le [FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="f1cc3-109">The profiler should provide the same `eltInfo` that it was given by the [FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md) function.</span></span>  
  
 `pFrameInfo`  
 <span data-ttu-id="f1cc3-110">[out] Handle opaque qui représente des informations génériques sur un frame de pile donné.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-110">[out] An opaque handle that represents generics information about a given stack frame.</span></span> <span data-ttu-id="f1cc3-111">Ce handle est uniquement valide pendant le rappel `FunctionEnter3WithInfo` au cours duquel le profileur a appelé la méthode `GetFunctionEnter3Info`.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-111">This handle is valid only during the `FunctionEnter3WithInfo` callback in which the profiler called the `GetFunctionEnter3Info` method.</span></span>  
  
 `pcbArgumentInfo`  
 <span data-ttu-id="f1cc3-112">[dans, out] Un pointeur vers la taille totale, en octets, de la [COR_PRF_FUNCTION_ARGUMENT_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-function-argument-info-structure.md) structure (plus supplémentaire [COR_PRF_FUNCTION_ARGUMENT_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-function-argument-range-structure.md) pour les plages d’argument vers lequel pointés `pArgumentInfo`).</span><span class="sxs-lookup"><span data-stu-id="f1cc3-112">[in, out] A pointer to the total size, in bytes, of the [COR_PRF_FUNCTION_ARGUMENT_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-function-argument-info-structure.md) structure (plus any additional [COR_PRF_FUNCTION_ARGUMENT_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-function-argument-range-structure.md) structures for the argument ranges pointed to by `pArgumentInfo`).</span></span> <span data-ttu-id="f1cc3-113">Si la taille spécifiée est insuffisante, ERROR_INSUFFICIENT_BUFFER est retourné et la taille attendue est stockée dans `pcbArgumentInfo`.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-113">If the specified size is not enough, ERROR_INSUFFICIENT_BUFFER is returned and the expected size is stored in `pcbArgumentInfo`.</span></span> <span data-ttu-id="f1cc3-114">Pour appeler `GetFunctionEnter3Info` pour récupérer uniquement la valeur attendue pour `*pcbArgumentInfo`, affectez à `*pcbArgumentInfo` la valeur 0 et à `pArgumentInfo` la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-114">To call `GetFunctionEnter3Info` just to retrieve the expected value for `*pcbArgumentInfo`, set `*pcbArgumentInfo`=0 and `pArgumentInfo`=NULL.</span></span>  
  
 `pArgumentInfo`  
 <span data-ttu-id="f1cc3-115">[out] Un pointeur vers un [COR_PRF_FUNCTION_ARGUMENT_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-function-argument-info-structure.md) structure qui décrit les emplacements des arguments de la fonction en mémoire, de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-115">[out] A pointer to a [COR_PRF_FUNCTION_ARGUMENT_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-function-argument-info-structure.md) structure that describes the locations of the function's arguments in memory, in left-to-right order.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f1cc3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f1cc3-116">Remarks</span></span>  
 <span data-ttu-id="f1cc3-117">Le profileur doit allouer suffisamment d'espace à la structure `COR_PRF_FUNCTION_ARGUMENT_INFO` de la fonction inspectée et indiquer la taille dans le paramètre `pcbArgumentInfo`.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-117">The profiler must allocate sufficient space for the `COR_PRF_FUNCTION_ARGUMENT_INFO` structure of the function that is being inspected, and must indicate the size in the `pcbArgumentInfo` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f1cc3-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f1cc3-118">Requirements</span></span>  
 <span data-ttu-id="f1cc3-119">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f1cc3-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f1cc3-120">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="f1cc3-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="f1cc3-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f1cc3-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f1cc3-122">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f1cc3-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1cc3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1cc3-123">See Also</span></span>  
 [<span data-ttu-id="f1cc3-124">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="f1cc3-124">FunctionEnter3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md)  
 [<span data-ttu-id="f1cc3-125">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="f1cc3-125">FunctionLeave3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md)  
 [<span data-ttu-id="f1cc3-126">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="f1cc3-126">FunctionTailcall3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)  
 [<span data-ttu-id="f1cc3-127">ICorProfilerInfo3, interface</span><span class="sxs-lookup"><span data-stu-id="f1cc3-127">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)  
 [<span data-ttu-id="f1cc3-128">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="f1cc3-128">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="f1cc3-129">Profilage</span><span class="sxs-lookup"><span data-stu-id="f1cc3-129">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
