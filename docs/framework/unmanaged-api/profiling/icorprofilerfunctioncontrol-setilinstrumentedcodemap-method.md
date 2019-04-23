---
title: ICorProfilerFunctionControl::SetILInstrumentedCodeMap, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionControl.SetILInstrumentedCodeMap
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionControl::SetILInstrumentedCodeMap
helpviewer_keywords:
- ICorProfilerFunctionControl::SetILInstrumentedCodeMap method [.NET Framework profiling]
- SetIILInstrumentedCodeMap method, ICorProfilerFunctionControl interface [.NET Framework profiling]
ms.assetid: ecf56646-7e5f-46c4-8340-f3a04e88920f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b36439dd6fb882bb41c38e953cb7b1c5f2b93d30
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59074103"
---
# <a name="icorprofilerfunctioncontrolsetilinstrumentedcodemap-method"></a><span data-ttu-id="833c0-102">ICorProfilerFunctionControl::SetILInstrumentedCodeMap, méthode</span><span class="sxs-lookup"><span data-stu-id="833c0-102">ICorProfilerFunctionControl::SetILInstrumentedCodeMap Method</span></span>
<span data-ttu-id="833c0-103">Définit une carte de code pour la fonction spécifiée à l’aide des entrées de mappage CIL (Common Intermediate Language) spécifiées.</span><span class="sxs-lookup"><span data-stu-id="833c0-103">Sets a code map for the specified function by using the specified Common Intermediate Language (CIL) map entries.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="833c0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="833c0-104">Syntax</span></span>  
  
```  
HRESULT SetILInstrumentedCodeMap(  
    [in]   ULONG      cILMapEntries,  
    [in, size_is(cILMapEntries)] COR_IL_MAP rgILMapEntries[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="833c0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="833c0-105">Parameters</span></span>  
 `cILMapEntries`  
 <span data-ttu-id="833c0-106">[en entrée] Le nombre d'entrées de la mappe.</span><span class="sxs-lookup"><span data-stu-id="833c0-106">[in] The number of entries in the map.</span></span>  
  
 `rgILMapEntries`  
 <span data-ttu-id="833c0-107">[in] Tableau d’entrées COR_IL_MAP allouée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="833c0-107">[in] The caller-allocated array of COR_IL_MAP  entries.</span></span> <span data-ttu-id="833c0-108">L’interprétation de ces entrées est le même que pour le [ICorProfilerInfo::SetILInstrumentedCodeMap](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setilinstrumentedcodemap-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="833c0-108">The interpretation of these entries is the same as for the [ICorProfilerInfo::SetILInstrumentedCodeMap](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setilinstrumentedcodemap-method.md) method.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="833c0-109">Notes</span><span class="sxs-lookup"><span data-stu-id="833c0-109">Remarks</span></span>  
 <span data-ttu-id="833c0-110">Définition du mappage en appelant cette méthode permet au débogueur de récupérer le mappage en appelant [ICorDebugILCode2::GetInstrumentedILMap](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-getinstrumentedilmap-method.md).</span><span class="sxs-lookup"><span data-stu-id="833c0-110">Setting the mapping by calling this method allows the debugger to retrieve the mapping by calling [ICorDebugILCode2::GetInstrumentedILMap](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-getinstrumentedilmap-method.md).</span></span> <span data-ttu-id="833c0-111">Elle permet aussi au débogueur d'utiliser le mappage en interne lors du calcul des décalages du langage intermédiaire pour les traces de pile et les cycles de vie des variables.</span><span class="sxs-lookup"><span data-stu-id="833c0-111">It also allows the debugger to use the mapping internally when calculating IL offsets for stack traces and variable lifetimes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="833c0-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="833c0-112">Requirements</span></span>  
 <span data-ttu-id="833c0-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="833c0-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="833c0-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="833c0-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="833c0-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="833c0-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="833c0-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="833c0-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="833c0-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="833c0-117">See also</span></span>

- [<span data-ttu-id="833c0-118">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="833c0-118">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
