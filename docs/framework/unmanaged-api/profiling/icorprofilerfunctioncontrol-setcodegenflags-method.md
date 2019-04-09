---
title: ICorProfilerFunctionControl::SetCodegenFlags, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionControl.SetCodegenFlags
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionControl::SetCodegenFlags
helpviewer_keywords:
- ICorProfilerFunctionControl::SetCodegenFlags method [.NET Framework profiling]
- SetCodegenFlags method, ICorProfilerFunctionControl interface [.NET Framework profiling]
ms.assetid: a2d5daa5-b990-4ae5-bf2a-c0862fe58bd7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 12f91bdd264135eb0ff3a48e15611cf5a0e3c064
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59104440"
---
# <a name="icorprofilerfunctioncontrolsetcodegenflags-method"></a><span data-ttu-id="5761f-102">ICorProfilerFunctionControl::SetCodegenFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="5761f-102">ICorProfilerFunctionControl::SetCodegenFlags Method</span></span>
<span data-ttu-id="5761f-103">Définit un ou plusieurs indicateurs à partir de la [COR_PRF_CODEGEN_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-codegen-flags-enumeration.md) fonction recompilée de l’énumération à la génération de code de contrôle pour un juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="5761f-103">Sets one or more flags from the [COR_PRF_CODEGEN_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-codegen-flags-enumeration.md) enumeration to control code generation for a just-in-time (JIT) recompiled function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5761f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5761f-104">Syntax</span></span>  
  
```  
HRESULT SetCodegenFlags(  
    [in] DWORD flags);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5761f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5761f-105">Parameters</span></span>  
 `flags`  
 <span data-ttu-id="5761f-106">[in] Un ou plusieurs indicateurs à partir de la [COR_PRF_CODEGEN_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-codegen-flags-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="5761f-106">[in] One or more flags from the [COR_PRF_CODEGEN_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-codegen-flags-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5761f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5761f-107">Remarks</span></span>  
 <span data-ttu-id="5761f-108">Le profileur obtient une instance de cette interface via la [ICorProfilerCallback4::GetReJITParameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="5761f-108">The profiler obtains an instance of this interface through the [ICorProfilerCallback4::GetReJITParameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md) callback.</span></span> `SetCodegenFlags` <span data-ttu-id="5761f-109">permet au profileur contrôler la génération de code pour la fonction recompilée.</span><span class="sxs-lookup"><span data-stu-id="5761f-109">allows the profiler to control the code generation for the recompiled function.</span></span> <span data-ttu-id="5761f-110">Comme avec tous les autres paramètres de recompilation JIT, les indicateurs de génération de code s’appliquent à toutes les instances de la fonction.</span><span class="sxs-lookup"><span data-stu-id="5761f-110">As with all other JIT recompilation parameters, the code generation flags apply to all instances of the function.</span></span>  
  
 <span data-ttu-id="5761f-111">Le compilateur JIT prend en compte ces indicateurs de compilation, ainsi que d’autres indicateurs spécifiés par d’autres sources, lors de la compilation d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="5761f-111">The JIT compiler considers these compilation flags, along with other flags specified by other sources, when compiling a function.</span></span>  <span data-ttu-id="5761f-112">Les autres sources incluent le débogueur, indicateurs globaux définie par le profileur au démarrage en utilisant le [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) (méthode) (avec les valeurs `COR_PRF_DISABLE_INLINING` et `COR_PRF_DISABLE_OPTIMIZATIONS`) et du profileur [ ICorProfilerCallback::JITInlining](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitinlining-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="5761f-112">The other sources include the debugger, global flags set by the profiler on startup by using the [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) method (with the values `COR_PRF_DISABLE_INLINING` and `COR_PRF_DISABLE_OPTIMIZATIONS`), and the profiler’s [ICorProfilerCallback::JITInlining](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitinlining-method.md) callback.</span></span>  <span data-ttu-id="5761f-113">Le compilateur JIT donne la priorité à une source qui demande le moins de l’optimisation.</span><span class="sxs-lookup"><span data-stu-id="5761f-113">The JIT compiler gives precedence to a source that requests the least amount of optimizing.</span></span>  <span data-ttu-id="5761f-114">Par exemple, si le profileur spécifie `COR_PRF_DISABLE_INLINING` au démarrage, mais ne spécifie ne pas `COR_PRF_CODEGEN_DISABLE_INLINING` dans le [ICorProfilerFunctionControl::SetCodegenFlags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) rappel, incorporation (inlining) est toujours désactivé.</span><span class="sxs-lookup"><span data-stu-id="5761f-114">For example, if the profiler specifies `COR_PRF_DISABLE_INLINING` on startup, but does not specify `COR_PRF_CODEGEN_DISABLE_INLINING` in the [ICorProfilerFunctionControl::SetCodegenFlags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) callback, inlining is still disabled.</span></span>  <span data-ttu-id="5761f-115">De même, si le profileur ne spécifie pas `COR_PRF_CODEGEN_DISABLE_INLINING` dans `SetCodegenFlags`, mais puis désactive la fonction inline à l’aide de la [ICorProfilerCallback::JITInlining](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitinlining-method.md) rappel, incorporation (inlining) est désactivé.</span><span class="sxs-lookup"><span data-stu-id="5761f-115">Similarly, if the profiler does not specify `COR_PRF_CODEGEN_DISABLE_INLINING` in `SetCodegenFlags`, but then disables inlining by using the [ICorProfilerCallback::JITInlining](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitinlining-method.md) callback, inlining is disabled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5761f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5761f-116">Requirements</span></span>  
 <span data-ttu-id="5761f-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5761f-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5761f-118">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5761f-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5761f-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5761f-119">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="5761f-120">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="5761f-120">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="5761f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5761f-121">See also</span></span>

- [<span data-ttu-id="5761f-122">ICorProfilerFunctionControl, interface</span><span class="sxs-lookup"><span data-stu-id="5761f-122">ICorProfilerFunctionControl Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-interface.md)
